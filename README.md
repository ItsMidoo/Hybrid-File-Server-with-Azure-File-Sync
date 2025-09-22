# Hybrid-File-Server-with-Azure-File-Sync
A step-by-step lab project demonstrating how to set up a hybrid file server with Azure File Sync, including Storage Account, File Share, Sync Group, Server Endpoint, Cloud Tiering, and Monitoring.

# Hybrid File Server with Azure File Sync

This project demonstrates how to configure a **Hybrid File Server** using **Azure File Sync**, enabling seamless synchronization between on-premises file servers and Azure File Shares.

## 📌 Overview
Azure File Sync allows you to:
- Centralize file shares in Azure while keeping local copies for fast access.
- Use **Cloud Tiering** to keep only frequently accessed files on-premises.
- Enable multi-site sync for branch offices.

This lab walks through:
- Creating a Storage Account & File Share
- Setting up a Sync Group
- Installing the Azure File Sync agent
- Creating a Server Endpoint
- Monitoring sync health and performance

---

## 🏗 Architecture

```mermaid
graph TD
     A[On-Premises File Server] -->|Azure File Sync Agent| B[Sync Group]
    B --> C[Azure File Share in Storage Account]
