## What is proper URLing in REST?
![enter image description here](https://img.shields.io/badge/Source-CHI%20Software-blue.svg)

Best practice is to use two url per resource: collection url and element url.

Suppose, we have `student` entity in our system.

    GET /students- Retrieves a list of students
    
    GET /students/12 - Retrieves a specific student
    
    POST /students- Creates a new student
    
    PUT /students/12 - Updates student #12
    
    PATCH /students/12 - Partially updates student #12
    
    DELETE /students/12 - Deletes student #12

