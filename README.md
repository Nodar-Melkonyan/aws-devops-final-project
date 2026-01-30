# Simple Python AWS DevOps Application

This is a minimal Python Flask application designed for an AWS DevOps final assessment.

## Routes

- `/` : Returns a simple text response to verify the application is running.
- `/db` : Attempts to connect to a database and run a simple query.

## Environment Variables

The application requires the following environment variables:

- DB_HOST
- DB_NAME
- DB_USER
- DB_PASSWORD

See `.env.example` for reference.

## Running Locally

```bash
pip install -r requirements.txt
python app.py
```

## AWS Usage

- Use Amazon RDS for the database.
- Deploy using ECS or EKS.
- Inject environment variables using task definitions or Kubernetes secrets.

# Simple Python AWS DevOps Application

ეს აპლიკაცია ემსახურება ორ ძირითად მიზანს:
1. შეამოწმოს ბოლო წერტილების სტატუსი (`/`). ამისთვის ის მარტივ მისალმებს აბრუნებს;
2. მონაცემთა ბაზის კავშირი შეამოწმოს (`/db`). ამოწმებს კავშირს Amazon RDS MySQL-ის მონაცემთა ბაზასთან და მოთხოვნის შედეგებს აბრუნებს.

მონაცემთა ბაზის კავშირისთვის აპლიკაცია იყენებს Flask-სა და PyMySQL-ს. კონფიგურაცია ხერხდება გარემოს ცვლადების მეშვეობით.

პროცესში გამოყენებული იქნება:
Amazon ECS კონტეინერის კოორდინაციისთვის;
Amazon RDS MySql ბაზისთვის;
Amazon ECR კონტაინერის სურათების სამართავად;
GitHub ქმედებები CI/CD-ის ავტომატიზაციისთვის;
ALB საჯარო წვდომისთვის.


## Repository Structure

aws-devops-final-project/
├── app.py # Main Flask application
├── requirements.txt # Python dependencies
├── README.md # This documentation file
└── .env.example # Environment variables template
