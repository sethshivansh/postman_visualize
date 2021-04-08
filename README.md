# postman_visualize
How to visualize or format the API response in POSTMAN.

### Definitions:

To format the API response specific attribute in formatted view to unscape the special character (\n) newline. 

Sample Response:

`{"first_name":"shivansh\nsecond_value\nthird\nfourth_value\nfinal value","last_name":"seth"}`

Data To format:

`"first_name":"shivansh\nsecond_value\nthird\nfourth_value\nfinal value"`

Expected Output:

![image](https://user-images.githubusercontent.com/55994712/114042268-e9d36000-98a2-11eb-9426-d27c3716304e.png)


## Steps to write Tests in POSTMAN

Please follow the below steps to run the script.

### Step-1 : 
open postman and enter the API endpoint whose response you want to format/visualize.

![image](https://user-images.githubusercontent.com/55994712/114040135-f5be2280-98a0-11eb-9b74-4a2c426f2c5d.png)

### Step-2 : 
Select the 'Tests' tab

![image](https://user-images.githubusercontent.com/55994712/114040058-e17a2580-98a0-11eb-919c-fb6a4eb701d7.png)

### Step-3 : 
Write the below script in "tests" tab

`pm.visualizer.set("<pre>{{text}}</pre>", {
    text: pm.response.json().first_name
});`

Here `first_name` is the API response JSON attribute which we are formatting.

![image](https://user-images.githubusercontent.com/55994712/114041783-75002600-98a2-11eb-97ae-546d53476a77.png)


### Step-4 : 

Run the API "send' and see the formatted output in 'Visualize' Tab.

![image](https://user-images.githubusercontent.com/55994712/114041349-1c308d80-98a2-11eb-814a-2e5ec9ae9a85.png)


