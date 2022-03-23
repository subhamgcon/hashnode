## Validate, Clean & Secure Your Kubernetes YAML With Validkube

# Why do we need tools like ValidKube?

For example when Developers write YAML files, to deploy their objects and they push their files to the git repository. Let's say it faced a failure in production. To detect the misconfigurations before it reaches production, tools like ValidKube comes in handy.

# What is ValidKube?

ValidKube combines the best open-source tools to help ensure Kubernetes YAML best practices, hygiene & security. It is a tool to **Clean**, **Validate** and **Secure** YAML files and makes a good developer experience while handling Kubernetes manifest files. 


![Screenshot 2022-03-23 at 11.40.19 PM.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1648059078156/qP9edH7Bv.png)

# How to use it?

Here is a sample YAML file provided by ValidKube to test the tool for the first time.

```
apiVersion: apps/v1
kind: Deployment
metadata:
  name: nginx-deployment
  namespace: example
  labels:
    app: nginx
spec:
  replicas: "Wrong"
  selector:
    matchLabels:
      app: nginx
  template:
    metadata:
      labels:
        app: nginx
    spec:
      containers:
      - name: nginx
        image: nginx:1.14.2
        args: []
        ports:
        - containerPort: 80
        resources: {}
```


By looking at it, you cannot determine the errors and misconfiguration present in the YAML file. That's where tools like ValidKube saves the day!

There are three ways ValidKube helps you to make your YAML file free of misconfiguration

## Validate 

Using ValidKube, you can Validate your YAML files. It can help you fix the indentation also add, remove and rearrange things according to the actual YAML and Kubernetes schema.

By running the provided YAML file by ValidKube, you will see this output:


![Screenshot 2022-03-23 at 11.47.05 PM.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1648059481717/rO1KpBAQR.png)


Here it shows that there is an error in the replicas section as in the given YAML file, replicas has a string value which is not correct as replicas can only have an Integer or a null value. You can see that in the output specified properly!
```
- errors:
  - 'spec.replicas: Invalid type. Expected: [integer,null], given: string'
  filename: /tmp/yaml/target_yaml.yaml
  kind: Deployment
  status: invalid
```
## Clean

Now let’s talk about how you can use the "Clean" feature of ValidKube to clean and enhance your YAML files with an instant click.

Here is a demo edited YAML file with some wrong arrangements and unnecessary keys:

```
apiVersion: apps/v1
kind: Deployment
metadata:
  name: nginx-deployment
  namespace: example
  labels:
    app: nginx
    
replicas: 2
spec:
  
  selector:
    matchLabels:
      app: nginx
  template:
    metadata:
      labels:
        app: nginx
    spec:
      containers:
      - name: nginx
        image: nginx:1.14.2
        args: []
        ports:
        - containerPort: 80
        resources: {}
```
Notice the resources key is unnecessary and has no value. Now when we run this file through the Clean feature we get this: 
 

![Screenshot 2022-03-24 at 12.26.20 AM.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1648061873144/Cj4BJM-dE.png)

```
apiVersion: apps/v1
kind: Deployment
metadata:
  labels:
    app: nginx
  name: nginx-deployment
  namespace: example
replicas: 2
spec:
  selector:
    matchLabels:
      app: nginx
  template:
    metadata:
      labels:
        app: nginx
    spec:
      containers:
      - image: nginx:1.14.2
        name: nginx
        ports:
        - containerPort: 80
```
Basically it helps us to get a more neat and clean version of the YAML file that we have provided!

## Secure

Kubernetes manifest needs to be secure and ValidKube helps us to achieve that with the help of the Aquasec team. The same YAML file mentioned above, we will run it through the "Secure" feature of ValidKube and let's see the results:


![Screenshot 2022-03-24 at 12.11.44 AM.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1648060970873/ItwK3-9ZP.png)

```
Results:
- Class: config
  MisconfSummary:
    Exceptions: 0
    Failures: 10
    Successes: 18
```
So our demo file has 10 failures or misconfiguration in it. Here Validkube comes in handy as it shows us what’s wrong with the security of our files and it also shows how to fix it with the reference docs which can refer further to fix the manifest files! Here is an example:

```
ID: KSV001
    IacMetadata: {}
    Layer: {}
    Message: Container 'nginx' of Deployment 'nginx-deployment' should set 'securityContext.allowPrivilegeEscalation'
      to false
    Namespace: appshield.kubernetes.KSV001
    PrimaryURL: https://avd.aquasec.com/appshield/ksv001
    Query: data.appshield.kubernetes.KSV001.deny
    References:
    - https://kubernetes.io/docs/concepts/security/pod-security-standards/#restricted
    - https://avd.aquasec.com/appshield/ksv001
    Resolution: Set 'set containers[].securityContext.allowPrivilegeEscalation' to
      'false'.
    Severity: MEDIUM
    Status: FAIL
    Title: Process can elevate its own privileges
    Type: Kubernetes Security Check
  - Description: The container should drop all default capabilities and add only those
      that are needed for its execution.
```

So that is how ValidKube by Komodor helps you Validate, Clean and Secure your Kubernetes YAML files without even downloading a tool, just by using your browser.

### Resources:

- [ValidKube](https://validkube.com/)

- [Contribute](https://github.com/komodorio/validkube)

- [Komodor](https://komodor.com/)


Consider following me on [Twitter](https://twitter.com/subhamstwt)

