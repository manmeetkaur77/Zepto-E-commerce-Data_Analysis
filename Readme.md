# Zepto E-commerce SQL Data Analysis Project

This project is a complete, end-to-end SQL Data Analyst Portfolio Project based on an e-commerce inventory dataset inspired by Zepto — one of India’s fastest-growing quick-commerce startups.

The project simulates how real data analysts work with messy retail data to explore, clean, and generate actionable insights.

## Project Overview

The main objectives of this project are to:

Create and manage an e-commerce inventory database in PostgreSQL

Perform Exploratory Data Analysis (EDA) to understand product categories, availability, and inconsistencies

Clean the dataset by handling nulls, removing invalid rows, and standardizing pricing

Generate business-driven insights on discounts, revenue, inventory, and product value

## Dataset Overview

Source: Public dataset inspired by Zepto’s product catalog (from Kaggle)

Unit of observation: Each row is a unique SKU (Stock Keeping Unit)

Key Details: Duplicate product names may appear in different package sizes, weights, or discounts — mimicking real-world retail catalogs.

## Columns

sku_id: Unique product identifier

name: Product name

category: Product category (Fruits, Snacks, Beverages, etc.)

mrp: Maximum Retail Price (converted from paise to ₹)

discount_percent: Discount applied on MRP

discounted_selling_price: Price after discount (₹)

available_quantity: Units available in inventory

weight_in_gms: Product weight in grams

out_of_stock: Boolean flag (True/False)

quantity: Units per package

## Project Workflow
### 1. Database & Table Creation

Designed schema with appropriate datatypes

Imported dataset into PostgreSQL using \copy

### 2. Data Exploration

Row counts, sample checks

Null value detection

Product category distribution

In-stock vs out-of-stock summary

Duplicate product detection

### 3. Data Cleaning

Removed rows with invalid pricing (mrp = 0 or selling_price = 0)

Converted prices from paise to rupees

Ensured consistent formatting

### 4. Business Analysis Queries

Top 10 best-value products (highest discount %)

High-MRP products currently out of stock

Estimated revenue by product category

Expensive products with minimal discounts

Top 5 categories by average discount

Price-per-gram analysis for value comparison

Product weight segmentation (Low, Medium, Bulk)

Total inventory weight per category

## Insights

Categories like Snacks and Beverages showed the highest discounts.

Certain high-MRP products (₹500+) were found to be frequently out of stock, indicating demand-supply mismatches.

Bulk-weight items contributed disproportionately to total inventory weight.

Price-per-gram analysis helped highlight best-value products for customers.

## Tech Stack

Database: PostgreSQL

Tools: pgAdmin / SQL Shell

Skills: SQL (DDL, DML, Joins, Aggregations, Window Functions, CASE statements)