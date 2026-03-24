# 🎬 NetflixData

A Data Warehouse solution designed for the storage, integration, and analysis of large-scale streaming data from Netflix. It centralizes structured information to support business intelligence, trend analysis, and data-driven decision-making.

## 📚 Managed Information

- 🎥 **Titles (Movies & TV Shows):**
   - 🆔 Title ID  
   - 📛 Name  
   - 📅 Release year  
   - 🎭 Genre  
   - ⏱️ Duration  
   - 🌍 Country  
   - 🗣️ Language  
   - 📝 Description  
- 👥 **Users:**
   - 🆔 User ID  
   - 📦 Subscription type  
   - 💰 Monthly revenue  
   - 📅 Join date  
   - 💳 Last payment date  
   - 🌎 Country  
   - 🎂 Age  
   - ⚧️ Gender  
   - 📱 Device  
- ⭐ **Reviews:**
   - 🆔 Review ID  
   - 👤 User ID  
   - 🎥 Title ID  
   - ⭐ Rating  
   - 📅 Review date  
   - 📝 Comments  
- 📈 **Stock Data:**
   - 📅 Date  
   - 💲 Open / Close  
   - 📊 High / Low  
   - 📦 Volume  
- 💹 **Financial Metrics:**
   - 📊 Daily stock behavior  
   - 📈 Market trends  

## 🚀 Features

- ⚙️ **Functionality:**
   - 🔄 ETL data integration processes  
   - ⚡ Fast query performance  
   - 📊 Data visualization and reporting  
   - 🔍 Trend and popularity analysis  
   - 🧠 Support for data-driven decisions  
   - ✔️ Data cleansing and validation  
- 📈 **Scalability:**
   - 📊 Handles large datasets  
   - 🧩 Flexible for new data sources  
   - 🔗 Integration with BI tools  
- 🛡️ **Security:**
   - 🔒 Structured data protection  
   - 🚫 Duplicate and inconsistency prevention  
   - 💾 Reliable storage mechanisms  

## 🧠 Data Warehouse Design

- 🧩 **Schema:** 
    - Star Schema  
- 📌 **Fact Tables:**
   - Reviews  
   - User activity  
   - Financial data  
- 📊 **Dimension Tables:**
   - Titles  
   - Users  
   - Time  
   - Country  
   - Genre  

## 🔄 Data Processing (ETL)

- 📥 **Extraction:**
   - CSV datasets  
- 🔧 **Transformation:**
   - Sorting records  
   - Removing duplicates  
   - Filtering null values  
   - Data type adjustments  
- 📤 **Loading:**
   - Integration into SQL Server  

## 🛠️ Technologies Used

- 🗄️ **Database:** Microsoft SQL Server  
- 🔄 **ETL Tool:** Pentaho Data Integration  
- 📊 **Visualization Service:** Power BI  
- 📂 **Data Source:** Kaggle  
- 🌱 **Version Control:** Git  

## ⚙️ Installation

### 📋 Prerequisites

- 🧰 [SQL Server Management Studio 2022](https://learn.microsoft.com/en-us/ssms/install/install)
- 🔄 [Pentaho Data Integration (Spoon)](https://pentaho.com/products/pentaho-data-integration/)
- 📊 [Power BI](https://www.microsoft.com/es-es/download/details.aspx?id=58494)

### ⚙️ Configuration

Follow these steps to set up the project:

📥 **Step 1: Clone the repository**

   ```bash
   git clone https://github.com/Crisrod0912/NetflixData.git
   ```

🔐 **Step 2: Configure database access**

   - Open **SQL Server Management Studio**.
   - Create a login in SQL Server that will be used to manage the Data Warehouse.
   
   Run the following commands in SQL Server Management Studio console:
   
   ```sql
   CREATE LOGIN db_connect WITH PASSWORD = 'your_password_here';
   ```

🗄️ **Step 3: Configure database**

   - Create a new database called `NetflixData`.
   - Import the provided SQL file `NetflixData.sql` into the `NetflixData` database using your server.

🛡️ **Step 4: Assign database user and permissions**

   After creating and importing the database, map the login to the database and grant the required permissions:

   ```sql
   USE NetflixData;

   CREATE USER db_connect FOR LOGIN db_connect;

   ALTER ROLE db_owner ADD MEMBER db_connect;
   ```

🔄 **Step 5: Run ETL processes**

   - Open Pentaho (Spoon)
   - Load .ktr files
   - Execute transformations

📊 **Step 4: Connect Power BI**

   - Connect to SQL Server
   - Load Data Warehouse tables
   - Build dashboards and reports
     - 📊 Data Sources
     - 📁 Netflix Movies and TV Shows
     - ⭐ Netflix Reviews
     - 👥 Netflix User Base
     - 📈 Netflix Stock Data
     - 💹 Financial Data

   All datasets are provided in CSV format and integrated into the Data Warehouse.

> [!NOTE]
> **Project Owner / Developer** 👨🏻‍💻  
>- Cristopher Rodríguez Fernández 
***
