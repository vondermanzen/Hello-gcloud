© The Chancellor, Masters and Scholars of The University of Oxford. All rights reserved.

# Explore different providers

This course is available for multiple cloud providers. Choose your preferred platform:

- [Hello Google Cloud](https://github.com/Oxford-Research-Cloud-Competency-Centre/Hello-gcloud) (You are here)
- [Hello Microsoft Azure](https://github.com/Oxford-Research-Cloud-Competency-Centre/Hello-azure)
- [Hello Amazon Web Services](https://github.com/Oxford-Research-Cloud-Competency-Centre/Hello-aws) (⭐ Most popular)
- [Hello IBM Cloud](https://github.com/Oxford-Research-Cloud-Competency-Centre/Hello-ibm-cloud)

# Instructions

<details>
<summary>Copy this repository (Optional: fork it)</summary>

<img width="417" height="369" alt="image" src="https://github.com/user-attachments/assets/0df56749-7f0c-49d0-a2a1-9691d635428f" />

***
</details>
<details>
<summary>Go to the Google Cloud Console and type "Cloud Run" in the search bar</summary>

<img width="1463" height="345" alt="img1" src="https://github.com/user-attachments/assets/e00ec6d6-94e3-46cd-8d42-5e9ae0d3c670" />

***
</details>
<details>
<summary>Go to Deploy Container -> Service</summary>

<img width="640" height="122" alt="img2" src="https://github.com/user-attachments/assets/c2358e8a-97d7-4c03-859f-5b6633dddc7a" />

***
</details>
<details>
<summary>Select "Continuously deploy from a repository (source or function)" then "Set up with Cloud Build"</summary>

<img width="1015" height="313" alt="img3" src="https://github.com/user-attachments/assets/c47e5487-5cc5-4f03-a25c-5129d0686d76" />

***
</details>
<details>
<summary>Select the git repository</summary>

<img width="566" height="438" alt="img4" src="https://github.com/user-attachments/assets/fc674a7f-ecca-4acf-91d4-642cfbb2d927" />

***
</details>
<details>
<summary>Select the "Google Cloud's buildpacks" option. Leave all the parameters empty: Cloud Run will figure out on its own that you are using Python.</summary>

<img width="553" height="491" alt="img5" src="https://github.com/user-attachments/assets/863344e1-0ed8-4177-b0a9-5c63d187438b" />

***
</details>
<details>
<summary>Select the region (europe-west2 in this case), allow unauthenticated invocations, allow internet traffic, then press Create</summary>

<img width="1045" height="815" alt="img6" src="https://github.com/user-attachments/assets/ce1bb06f-f59e-4903-b55d-963c546c8d32" />

***
</details>
The app should now be publicly accessible.

<img width="623" height="352" alt="img7" src="https://github.com/user-attachments/assets/d1f89a7d-0a66-4282-b382-543759107ab9" />

# Going further

<details>
<summary><h2>Modifying the code</h2></summary>

You can commit some changes to your repository and watch how the service is updated automatically. 

</details>

<details>
<summary><h2>Cleaning up</h2></summary>

Don't forget to delete the service when you are done.

<img width="415" height="170" alt="delete" src="https://github.com/user-attachments/assets/66a67610-3ea0-4aa8-a864-0f3a44131e32" />

</details>

<details>
<summary><h2>Adding an API endpoint</h2></summary>

Add the following code in app.py

```	
@app.route("/hello_api")
def hello_api():
    return {
		"name": "Wrinkle Five Star",
		"species": "Duck",
		"breed": "American Pekin",
		"hatching_date": "2020-09-09",
		"sex": "Male"
    }
```

Then test your endpoint

<img width="545" height="186" alt="hello_api" src="https://github.com/user-attachments/assets/d9983062-6360-4751-9b52-40776a5fee38" />

</details>

<details>
<summary><h2>Local testing</h2></summary>

You need to test your changes before publishing them. 

<details>
<summary>Install Python</summary>

```	
https://www.python.org/downloads/
```

***
</details>
<details>
<summary>Install dependencies</summary>

```	
python -m pip install --break-system-packages -r requirements.txt
```

***
</details>
<details>
<summary>Run flask</summary>

```	
python -m flask run --port=80
```

Open localhost in your browser.   

***
</details>

<img width="231" height="125" alt="image" src="https://github.com/user-attachments/assets/b6213fd9-344e-4223-b8dd-8cc192b2403a" />

</details>
