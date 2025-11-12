# Functional and Use Case Documentation

## 1. Introduction

## 1.1 Project Overview

### Problem Statement

Many individuals face challenges in tracking their daily expenses and maintaining control over their financial activities. Traditional methods such as using notebooks or spreadsheets are inefficient, prone to human error, and lack analytical insights. Without a clear overview of income and expenditure, users often struggle to identify spending patterns, manage savings, or make informed financial decisions.

### Project Overview

The **Personal Expense Tracker** is a **web-based and mobile-accessible application** that enables users to manage income and expenses effectively through an **intuitive dashboard interface**.  
It provides a **central overview page** displaying monthly income, monthly expenses (with a pie chart), last month’s pie chart, and recent transactions.  

The system is designed as a **Progressive Web App (PWA)** to ensure responsive, cross-platform usability with secure storage, and fast load times.

It empowers individuals to maintain financial awareness, analyze spending habits, and generate **monthly transaction reports in PDF format**. A **CI/CD pipeline** ensures deployment quality, and integrated QA practices maintain system reliability.

---

## 1.2 Purpose

The purpose of this project is to empower individuals to take control of their financial habits by providing a reliable, secure, and user-friendly tool for tracking daily income and expenses.

---

## 1.3 Target Audience

This application is intended for **individual users** who want a clear, simple way to manage their expenses and analyze monthly spending patterns.

---

## 1.4 Goals

- Enable users to log and manage their daily expenses easily.  
- Provide visual insights into spending habits.  
- Help users download and review their expense summaries.

---

## 2. Project Objectives

## 2.1 Simplify and Centralize Expense Management

To simplify the management of daily expenses or financial data, the system keeps the record of all income and expenses into a single dashboard. There is no need to manually maintain the records.

---

## 2.2 Record Income and Expenses through Categorized Transactions

Users can input transactions under various predefined categories (e.g., Food, Travel, Bills, Savings).  
This categorization enhances organization and allows for precise tracking of spending behavior.

---


## 2.3 Offer Cross-Platform Access via PWA

The system is implemented as a **Progressive Web App (PWA)**, enabling seamless use across web and mobile devices.  

---

## 2.4 Maintain Secure and Reliable Storage Using PostgreSQL

PostgreSQL provides a powerful and reliable relational database solution for structured data management.
It ensures data integrity, security, and scalability while efficiently handling user transactions, authentication details, and application-related records.
Its ACID compliance and robust query capabilities make it ideal for maintaining accurate financial records in the Personal Expense Tracker.

---

## 2.5 Implement CI/CD, Manual Testing, and Security Scans

A CI/CD pipeline automates deployment and updates, ensuring code quality and reliability.  
Manual testing and security scans are conducted regularly to identify bugs, improve performance, and maintain overall system security.

---

**Next:** [Scope →](scope.md)
