# DevSecOps-StarterKit: Elevate Your CI/CD Security

Welcome to **DevSecOps-StarterKit**! This repository is your springboard to seamlessly infusing vital security checks into the Software Development Life Cycle (SDLC). Tailored for developers, especially those fresh to the security realm, we offer out-of-the-box templates for leading pipeline solutions: GitHub Actions, Azure DevOps Pipelines, and GitLab CI. Dive into our comprehensive suite of security analyses:

Our mission is straightforward: to simplify the integration of baseline security checks, ensuring a robust and secure software delivery. Embrace, adapt, and bolster these templates to foster a safer coding environment!

# DevSecOps StarterKit 🛡️

Welcome to the **DevSecOps StarterKit**! This repository serves as a launchpad for small teams and projects that might not have in-depth cybersecurity knowledge but understand the importance of integrating security into their development pipeline. By leveraging this kit, teams can seamlessly introduce robust security scanning into their CI/CD workflows.

## 🌟 Features:
- **Pre-configured Pipelines**: Ready-to-use configurations for popular CI/CD platforms: GitLab CI, Azure DevOps, and GitHub Actions.
- **Comprehensive Scans**: The kit incorporates a variety of security scans, including SAST, Dependency Scans, Image Scans, and Infrastructure-as-Code (IaC) evaluations.
- **Flexibility**: Whether you're pulling from a public container registry, building a local image, or scanning infrastructure code, we've got you covered with optional steps and clear documentation.

## 🛠️ Included Security Scans:

### 1. **SAST Scan (Static Application Security Testing)**:
   - **Description**: SAST is a testing process that analyzes source code, bytecode, or binary code of your application for security vulnerabilities, typically without executing it. It helps identify areas where you may have used patterns known to be insecure.
   - **Tool Used**: [Semgrep](https://semgrep.dev/)

### 2. **Dependency Scan**:
   - **Description**: Scans dependencies of your projects for known vulnerabilities. It ensures that the libraries and other dependencies you're using do not contain security flaws.
   - **Tool Used**: [OWASP Dependency-Check](https://github.com/jeremylong/DependencyCheck)

### 3. **Image Scan**:
   - **Description**: Scans Docker container images for vulnerabilities. Ensures that the underlying software and OS layers of your containers do not have known security issues.
   - **Tool Used**: [Trivy](https://github.com/aquasecurity/trivy)

### 4. **Infrastructure-as-Code (IaC) Scan**:
   - **Description**: Analyzes your Infrastructure-as-Code templates for security misconfigurations and compliance violations. Ensures that your infrastructure provisioning scripts adhere to best security practices.
   - **Tool Used**: [Checkov](https://www.checkov.io/)

### 5. **Secrets Scan**:
   - **Description**: Scans the repository for secrets accidentally committed, like passwords, API keys, and tokens. Helps ensure that sensitive information is not inadvertently exposed.
   - **Tool Used**: [TruffleHog](https://github.com/trufflesecurity/trufflehog)

Remember, each scan is important in its own way, addressing different aspects of application and infrastructure security. Using them in tandem ensures a more comprehensive security evaluation for your projects.

## 📋 Prerequisites:

For the **DevSecOps StarterKit** to function seamlessly, there's only one primary requirement:

### Docker Support 🐳:
- All the security scans included in this kit utilize Docker containers. Therefore, ensure that your CI/CD runner is capable of executing Docker commands.
- Good news! Most modern CI/CD platforms, including GitLab CI, Azure DevOps, and GitHub Actions, have built-in support for Docker by default. This means you can typically use the StarterKit without any additional runner configuration.

Before integrating any pipeline from this kit, ensure your CI/CD environment has Docker installed and configured. If you're using a custom runner, verify that Docker is accessible to it.

By keeping Docker as the sole dependency, we aim to make the integration process smooth and the entry barrier minimal for teams of all sizes.

## 🚀 Getting Started:
1. Choose your platform directory (GitLab CI, Azure DevOps, or GitHub Actions).
3. Copy the given template into your project files. 
4. Make sure you change the default docker image for the one you want to scan in the variables section. If you want to scan your own built image, uncomment the section made for that purpose under the Image Scan section.
5. Integrate the pipeline configuration into your project, and go to the pipeline section to run it. You are set to go!

## 💡 Why DevSecOps?
Security is often treated as an afterthought, but with the rise in cyber threats, it's crucial to integrate security measures right from the development phase. DevSecOps bridges the gap between development and security, ensuring faster releases without compromising on security.

## Support and Contributions:
Feel free to raise issues if you encounter any problems or have suggestions. Contributions via pull requests are more than welcome to enhance the capabilities of this StarterKit.

_Equip your team with the power of security from the get-go. Dive in and safeguard your projects with the DevSecOps StarterKit!_
