**Создать запросы в Postman.**
  
**Protocol: http**  
**IP: 162.55.220.72**  
**Port: 5005**  
  
EP_1  
Method: GET  
EndPoint: /get_method  
request url params:  
 name: str  
 age: int  
  
response:  
[  
	“Str”,  
	“Str”  
]  
  
```
Прописываем в окружение ip:, port:162.55.220.72, name:Alexander, age:43.  
В строке запроса выбираем метод GET и пишем путь к эндпойнту:  
http://{{ip}}:{{port}}/get_method  
  
В параметрах запроса прописать:  
age: {{age}}  
name: {{name}}  
  
Сохранить, послать запрос.  
В результатах запроса:  
[  
	"Alexander",  
	"43"  
]  
```
  
  
==================  
  
EP_2  
Method: POST  
EndPoint: /user_info_3  
request form data:  
 name: str  
 age: int  
 salary: int  
  
response:  
{'name': name,  
		  'age': age,  
		  'salary': salary,  
		  'family': {'children': [['Alex', 24], ['Kate', 12]],  
					 'u_salary_1_5_year': salary * 4}}  
  
  
```
В окружение дописываем salary:1000  
В строке запроса выбираем метод POST и пишем путь к эндпойнту:  
http://{{ip}}:{{port}}/user_info_3  
  
Перейти во вкладку body.  
В form-data прописать:  
age: {{age}}  
name: {{name}}  
salary: {{salary}}  
  
Сохранить, послать запрос.  
В результатах запроса:  
{  
	"age": "43",  
	"family": {  
		"children": [  
			[  
				"Alex",  
				24  
			],  
			[  
				"Kate",  
				12  
			]  
		],  
		"u_salary_1_5_year": 4000  
	},  
	"name": "Alexander",  
	"salary": 1000  
}  
```
  
  
==================  
 
EP_3  
Method: GET  
EndPoint: /object_info_1  
request url params:  
 name: str  
 age: int  
 weight: int  
 
response:  
{'name': name,  
		  'age': age,  
		  'daily_food': weight * 0.012,  
		  'daily_sleep': weight * 2.5}  
 
 
```
В окружение дописываем weight:1000  
В строке запроса выбираем метод GET и пишем путь к эндпойнту:  
http://{{ip}}:{{port}}//object_info_1  
 
В параметрах запроса прописать:  
age: {{age}}  
name: {{name}}  
weight: {{weight}}  
 
Сохранить, послать запрос.  
В результатах запроса:  
 
{  
	"age": 43,  
	"daily_food": 1.2,  
	"daily_sleep": 250.0,  
	"name": "Alexander"  
}  
```
 
 
==================  
  
EP_4  
Method: GET  
EndPoint: /object_info_2  
request url params:  
 name: str  
 age: int  
 salary: int  
 
response:  
{'start_qa_salary': salary,  
		  'qa_salary_after_6_months': salary * 2,  
		  'qa_salary_after_12_months': salary * 2.7,  
		  'qa_salary_after_1.5_year': salary * 3.3,  
		  'qa_salary_after_3.5_years': salary * 3.8,  
		  'person': {'u_name': [user_name, salary, age],  
					 'u_age': age,  
					 'u_salary_5_years': salary * 4.2}  
		  }  
 
 
```
В строке запроса выбираем метод GET и пишем путь к эндпойнту:  
http://{{ip}}:{{port}}//object_info_2  
 
В параметрах запроса прописать:  
age: {{age}}  
name: {{name}}  
salary: {{salary}}  
 
Сохранить, послать запрос.  
В результатах запроса:  
 
{  
	"person": {  
		"u_age": 43,  
		"u_name": [  
			"Alexander",  
			1000,  
			43  
		],  
		"u_salary_5_years": 4200.0  
	},  
	"qa_salary_after_1.5_year": 3300.0,  
	"qa_salary_after_12_months": 2700.0,  
	"qa_salary_after_3.5_years": 3800.0,  
	"qa_salary_after_6_months": 2000,  
	"start_qa_salary": 1000  
}  
```
  
 
==================  
 
EP_5  
Method: GET  
EndPoint: /object_info_3  
request url params:  
 name: str  
 age: int  
 salary: int  
 
response:  
{'name': name,  
	  'age': age,  
	  'salary': salary,  
	  'family': {'children': [['Alex', 24], ['Kate', 12]],  
					 'pets': {'cat':{'name':'Sunny',  
									 'age': 3},  
							  'dog':{'name':'Luky',  
									 'age': 4}},  
					 'u_salary_1_5_year': salary * 4}  
		  }  
 
 
```
В строке запроса выбираем метод GET и пишем путь к эндпойнту:  
http://{{ip}}:{{port}}//object_info_3  
 
В параметрах запроса прописать:  
age: {{age}}  
name: {{name}}  
salary: {{salary}}  
 
Сохранить, послать запрос.  
В результатах запроса:  
{  
	"age": "43",  
	"family": {  
		"children": [  
			[  
				"Alex",  
				24  
			],  
			[  
				"Kate",  
				12  
			]  
		],  
		"pets": {  
			"cat": {  
				"age": 3,  
				"name": "Sunny"  
			},  
			"dog": {  
				"age": 4,  
				"name": "Luky"  
			}  
		},  
		"u_salary_1_5_year": 4000  
	},  
	"name": "Alexander",  
	"salary": 1000  
}  
```

 
==================  
 
EP_6  
Method: GET  
EndPoint: /object_info_4  
request url params:  
 name: str  
 age: int  
 salary: int  
 
response:  
{'name': name,  
		  'age': int(age),  
		  'salary': [salary, str(salary * 2), str(salary * 3)]}  
 
  
```
В строке запроса выбираем метод GET и пишем путь к эндпойнту:  
http://{{ip}}:{{port}}//object_info_4  
 
В параметрах запроса прописать:  
age: {{age}}  
name: {{name}}  
salary: {{salary}}  
 
Сохранить, послать запрос.  
В результатах запроса:  
{  
	"age": 43,  
	"name": "Alexander",  
	"salary": [  
		1000,  
		"2000",  
		"3000"  
	]  
}  
```
 
 
==================  
 
EP_7  
Method: POST  
EndPoint: /user_info_2  
request form data:  
 name: str  
 age: int  
 salary: int  
 
response:  
{'start_qa_salary': salary,  
		  'qa_salary_after_6_months': salary * 2,  
		  'qa_salary_after_12_months': salary * 2.7,  
		  'qa_salary_after_1.5_year': salary * 3.3,  
		  'qa_salary_after_3.5_years': salary * 3.8,  
		  'person': {'u_name': [user_name, salary, age],  
					 'u_age': age,  
					 'u_salary_5_years': salary * 4.2}  
		  }  
 
```
В строке запроса выбираем метод POST и пишем путь к эндпойнту:  
http://{{ip}}:{{port}}/user_info_2  
 
Перейти во вкладку body.  
В form-data прописать:  
age: {{age}}  
name: {{name}}  
salary: {{salary}}  
 
Сохранить, послать запрос.  
В результатах запроса:  
{  
	"person": {  
		"u_age": 43,  
		"u_name": [  
			"Alexander",  
			1000,  
			43  
		],  
		"u_salary_5_years": 4200.0  
	},  
	"qa_salary_after_1.5_year": 3300.0,  
	"qa_salary_after_12_months": 2700.0,  
	"qa_salary_after_3.5_years": 3800.0,  
	"qa_salary_after_6_months": 2000,  
	"start_qa_salary": 1000  
}  
```
