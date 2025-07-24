# Multi-Cloud IAM Hardening Project

This project demonstrates how to implement secure Identity and Access Management (IAM) across AWS, GCP, and Azure. Phase 1 focuses on AWS and includes real-world practices like enforcing MFA, applying least privilege, and using Access Analyzer.

---

## 🔐 Phase 1: AWS IAM Hardening

### ✅ Objectives
- Create custom least-privilege IAM policies
- Set up PowerUser access using AWS-managed policies
- Enforce MFA for all IAM users
- Apply a strong password policy
- Use IAM Access Analyzer to detect risky permissions
- Secure specific AWS services (S3, EC2)

---

## 📂 Folder Structure

multi-cloud-iam-hardening/
├── aws/
│ ├── screenshots/ # Screenshots showing IAM configurations
│ ├── least-privilege-ec2-s3.json # Custom IAM policy for EC2 & S3 read access
│ ├── least-privilege-policy-notes.md
│ └── poweruser-access-notes.md
├── README.md # This file


---

## 📄 Project Components

### 🔸 `least-privilege-ec2-s3.json`
A JSON policy that grants:
- Read-only access to EC2 (e.g., DescribeInstances)
- Read access to a specific S3 bucket

### 🔸 `least-privilege-policy-notes.md`
Detailed walkthrough on how the least-privilege policy was created and applied in AWS IAM, including:
- User testing
- Policy logic
- Security rationale

### 🔸 `poweruser-access-notes.md`
Explains the use of the AWS-managed `PowerUserAccess` policy and why it's appropriate for mid-level roles that don't require IAM privileges.

### 🔸 `screenshots/`
Contains visual proof of key configurations:
- Password policy settings
- MFA enforcement
- IAM group and user setup
- Access Analyzer findings

---

## 🧪 Testing

IAM permissions were tested by logging in with different IAM users:
- Verified EC2 and S3 access granted by custom policies
- Confirmed IAM or unauthorized actions were blocked
- Used Access Analyzer to catch any unintended exposures

---

## 🚀 Next Steps

- [ ] Phase 2: GCP IAM Hardening
- [ ] Phase 3: Azure IAM Hardening
- [ ] Add Terraform scripts to automate policy creation
- [ ] Add multi-cloud audit and SIEM integration

---

## 👨‍💻 Author

**James Leverett**  
Cybersecurity & Cloud Enthusiast  
[LinkedIn Profile](https://www.linkedin.com/in/james-leverett-5452aa18b/)

---

## 📜 License

This project is open source and available under the [MIT License](LICENSE).


