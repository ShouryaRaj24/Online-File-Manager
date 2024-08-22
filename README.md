# File Upload and Download API

This Spring Boot application allows users to upload files and download them using various endpoints.

## Endpoints

### 1. **Upload Files**
- **POST** `http://localhost:8080/upload-file`
- **Request Body:** 
  - Type: `form-data`
  - Key: `file`
  - Value: [Select your file(s) to upload]

### 2. **Download Files**
- **GET** `http://localhost:8080/download`
- **Query Parameters:**
  - Key: `fileName`
  - Value: `example.pdf`
  
  **OR**

  In your browser: [http://localhost:8080/download?fileName=example.pdf](http://localhost:8080/download?fileName=example.pdf)

### 3. **Download Files Faster**
- **GET** `http://localhost:8080/download-faster`
- **Query Parameters:**
  - Key: `fileName`
  - Value: `example.pdf`
  
  **OR**

  In your browser: [http://localhost:8080/download-faster?fileName=example.pdf](http://localhost:8080/download-faster?fileName=example.pdf)

## Frontend Integration

### 1. **File Uploader**
To see the file uploader interface, open your browser and go to: [http://localhost:8080/uploader](http://localhost:8080/uploader)

### 2. **List Files**
To view and download files from the directory, go to: [http://localhost:8080/list-files](http://localhost:8080/list-files)

## ChatGPT Prompts for HTML Templates

### **Uploader Page (`uploader.html`)**

**Prompt:**  
```
I want to create a single page html, css, and js that will provide an option to upload a file. Make it pretty with CSS styling. The endpoint for upload is "/upload-file" with the file submitted as Multipartfile with the param name "file". I have attached the Spring Boot file upload endpoint. I want CSS + HTML + JS in one single HTML file.
```

### **List Files Page (`list_files.html`)**

**Prompt:**  
```
Generate a Thymeleaf template that lists all files within a directory. When a row is clicked, I want to download the file using the api/download-faster with the GET parameter fileName. I have attached the controller method signature.
```


### **To see with the Frontend**
**In Browser type:**

- [http://localhost:8080/list-files](http://localhost:8080/list-files)  
- [http://localhost:8080/uploader](http://localhost:8080/uploader)


