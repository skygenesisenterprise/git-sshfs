# Git SSHFS Tools System

Git SSHFS Tools System is an experimental open-source tool designed to simplify remote development and compilation workflows.  
It combines the power of **Git** for source code management with **SSHFS** (SSH File System) to create seamless shared workspaces between local and remote environments.

---

## 🚀 Features
- **Git + SSHFS integration**: Automatically synchronize your Git repository with a remote server through SSHFS.
- **Remote compilation**: Code locally, compile remotely on powerful servers without the need to clone repositories manually.
- **Shared sessions**: Work as if you were directly on the server while keeping your development environment local.
- **Lightweight & secure**: Uses native SSH encryption and efficient sync mechanisms.
- **Cross-platform**: Works on Linux, macOS, and (planned) Windows WSL2.

---

## 📦 Installation
> ⚠️ This project is in early development and not yet available as a packaged release.

Clone the repository:
```bash
git clone https://github.com/skygenesisenterprise/git-sshfs.git
cd git-sshfs
```

Install dependencies (example for Node.js / TypeScript implementation):

```bash
npm install
```

Build the project:

```bash
npm run build
```

---

## 🛠 Usage

Mount a Git repository into a remote server via SSHFS:

```bash
git sshfs connect user@remote-server:/path/to/project
```

Start a shared compilation session:

```bash
git sshfs build --remote
```

Disconnect:

```bash
git sshfs disconnect
```

---

## 📚 Roadmap

* [ ] Initial CLI prototype in TypeScript
* [ ] Auto-sync with Git events (commit, push, fetch)
* [ ] Remote build orchestration
* [ ] VSCode / JetBrains integration
* [ ] Windows support (via WSL2)
* [ ] Multi-user collaborative sessions

---

## 🤝 Contributing

Contributions are welcome!
Please fork the repository, create a new branch, and submit a pull request.

---

## 📄 License

This project is licensed under the **Apache 2.0 licence**.
See [LICENSE](LICENSE) for details.
