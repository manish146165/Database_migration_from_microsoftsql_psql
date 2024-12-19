Postgresql and MSSQL SERVER SETUP ON LINUX UBUNTU-22.04

&  
Database Migration From Mssql to Psql

  
  

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfmgd_C0_LO9P-7ks1cPkpNNh2xEd8hBBkL7zYx2hiMEBiIaNJqPDVoeDiDnJrQa1CKjfxJdaVcRpt9PhyQA0mZMBm_Klk5kuSakMWiAjTagIBUkhu2cJE9k0281GQkS7j50Y9ORRvSJwDdzyuosHhkcZxs?key=VKRitSN_Nk2iZ-d42Pg8vQ)

  
  

Microsoft SQL Server (MSSQL) is a relational database management system (RDBMS) developed by Microsoft. It is a powerful and widely used database server that provides a secure and scalable platform for storing and retrieving data.

  
  

To install the SQL Server Express Edition, the first step is to go to the official Microsoft SQL website and download the Express Edition from there.

  

To download SQL Server on Linux for Ubuntu, click on the link provided below:

[https://learn.microsoft.com/en-us/sql/linux/quickstart-install-connect-ubuntu?view=sql-server-ver16&tabs=ubuntu2204](https://learn.microsoft.com/en-us/sql/linux/quickstart-install-connect-ubuntu?view=sql-server-ver16&tabs=ubuntu2204)

  
  
  

Here are the steps below that I used to set up Microsoft SQL.

  

Step1. curl -fsSL https://packages.microsoft.com/keys/microsoft.asc | sudo gpg --dearmor -o /usr/share/keyrings/microsoft-prod.gpg

This command is used to download and import the Microsoft GPG (GNU Privacy Guard) key for package verification.

  
  

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeUON45uDDoNQoUdibcdpxpFTPnrtO9UMPX6jho_jGS8M6uvbWHqr1bPJl7y3oa7utV7iooNm77y3qGbrdI6rXJ9iLAOGieO0bWpfa5B0dMUf8z_fz_dapIzVZpFoJEhimQsRMSd5-PiGRRGr9nCObFYKPQ?key=VKRitSN_Nk2iZ-d42Pg8vQ)

  
  

Step2.  curl https://packages.microsoft.com/keys/microsoft.asc | sudo tee /etc/apt/trusted.gpg.d/microsoft.asc

  

This command is used to download the Microsoft GPG (GNU Privacy Guard) key and add it to the system's trusted GPG keyring for APT (Advanced Package Tool), which is used by Debian-based package management systems such as Ubuntu. 

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfODqrML4iZ2W7U_oVuFcEDohUFxqd2RzY7pxCJtEj5VKjPvsZFKClZZS7eqOUTdpyprwIt6FdLWXxqoXOC7sBZiDhBc9lhNDTMI9TgdgxgNnjrjAs5UCtHpOrSUp1MGC1lfnOhx4gPacT9YiMw-gHQNFI?key=VKRitSN_Nk2iZ-d42Pg8vQ)

  
  

Step3. curl -fsSL https://packages.microsoft.com/config/ubuntu/22.04/mssql-server-2022.list | sudo tee /etc/apt/sources.list.d/mssql-server-2022.list

  

This command is used to download a configuration file for Microsoft SQL Server 2022 and then add the contents of that file to a specific list file in the /etc/apt/sources.list.d/ directory.

  

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcagIgMMgWSNS8lnVdsVDRsV_vg23djmVvGxBNHN7LFYz04WKSPW7INJLgxA3d4Ybo1efoBs8p9pwdWNmE8__xu3wLSpgrPcn9-KaKjnaXzh_DzVO7wcl1kXTCKx8-8wAcU3gDmYFAcG-pIyNMz-7Om6sy5?key=VKRitSN_Nk2iZ-d42Pg8vQ)

  
  
  
  
  

Step4.  sudo apt update

  

The sudo apt update command is used to update the local package index on a Debian-based Linux system. 

  

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXe9Fd3hn6g28rMG0In7dqCTeF0vqmyGhQNUTXYHeZw0sMf-9rtF-UoHS0TtD9HcZD31a6JeusolC03tFWLaMOXAtXfWbj8PIB7FZzlyhnF8D0aPBx3oUJO6ArU_nT4jBEtcrAohfwbLjpFOgK8RAAik61J9?key=VKRitSN_Nk2iZ-d42Pg8vQ)

  
  

Step5. sudo apt-get install -y mssql-server

  

This command is used to install Microsoft SQL Server on a Debian-based Linux system using the apt-get package management tool.

  

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdtaWRvI9Pcgt4Rdf9Ahp5ayt580ow-GD7FZwFwSe4kJh8DdusonK7YS5fQI6Q5E9o93RwGKBa9gyLleFvcqy7edKJTD4-slknISGBI-v6ZOptG9QKnXrx83LaAqYktqrwatEzzfcSiVLwv-biRhLzVyloL?key=VKRitSN_Nk2iZ-d42Pg8vQ)

  
  

Step6. sudo /opt/mssql/bin/mssql-conf setup

  

This command is used to launch the setup process for Microsoft SQL Server on Linux.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfNsWvTeso68cXLmB5rQ-YruLTuvu8CR5Jv5mhJSI90DY3WjZKVyWrUvNJO-c1W022nNbk2Qc04p_n9yHillfsF2tsIuWrWgrEhI1He4-g2TeLZJ_3EFuHaLl6hU5lYeABwAwXSNxLN5hYqTCLbnq0jz9gr?key=VKRitSN_Nk2iZ-d42Pg8vQ)

  
  

Step7. systemctl status mssql-server --no-pager

  

This command is used to check the status of the Microsoft SQL Server service using systemctl, a Linux command for examining and controlling the state of the system's init system and service manager.

  

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXf1D2gWbdC37O675ACTy_76dv7CjmD3ExsW2gpQ202qm8KzTZUpUvXemd0Pn0nkcfrVznMCb11AgsmG6tZIMtfSn9MZQValiD9zYVfI8hD71fwK8yLE731xVZ6l5Mh3n45YvuY9tKB3Pw9jdz2VGlpV-PPo?key=VKRitSN_Nk2iZ-d42Pg8vQ)

  
  

 If you plan to connect remotely, you might also need to open the SQL Server TCP port (default 1433) on your firewall.

  

Step1. sudo apt-get install ufw

  

The sudo apt-get install ufw command is used to install the Uncomplicated Firewall (UFW) on a Debian-based Linux system, such as Ubuntu.

  

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXe3qspIZYuSoVOFR_s_hCJzAIcXnjX8o3xk83l_gevUaj_ggedq11H2E8nv3foRtf_6a18Qqn95MdHXqdt_xOMXBOlRKHkQkxs1zV9MQispTBYTxVh1giNiFdFQx9UXRLef8k0w7rnEt9oQMa4CxZddHHLd?key=VKRitSN_Nk2iZ-d42Pg8vQ)

  

Step2.  sudo ufw enable

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXd_NqIHJQji_3iThXnZdmaaNQea6Ub5Bh24btEVxuLJw7IZj9ZjL2tsCdi1cJZD-7H0h9E5qK9PNcB94tj1ijHhUknXwqkOcqTWniYyKMkleBeZRXTSpQUpUJdbR7CYKZEwAehj-1LkHv5IeP8_edgnPQ8?key=VKRitSN_Nk2iZ-d42Pg8vQ)

  

Step3. sudo ufw allow 1433/tcp

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeETYpnbLggy3sWh7S8kNmsYvcfCxtUFzFysqnU7kUWtIjp3XOWuHij7q4QlMfOtKsA3g40TPnTRjYYX-E2kCO9O5uQFA-C7Xoi2DNW7ke9DLoBkuqfOyTj1ZCsRHi6ruuVZ0JZeCQ5wzcAuhOcPv0WnyGS?key=VKRitSN_Nk2iZ-d42Pg8vQ)

  

Step4. sudo ufw status

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdlLUzLHASmGIpZoj6rPWkDie2zK23CUwbs32nbZcTnlSuBeqyl3KpGrcA6_dC6fFAJTUNrPUmLI6AdpdGBicUzJXXXzznNV5lNeJxQfgFtH_5-UeyxJSIRDsb3xJma13J59jRvhT72Ko_mKiAuJYSxQ_Gr?key=VKRitSN_Nk2iZ-d42Pg8vQ)

## Download and install sqlcmd

  

Step1. curl https://packages.microsoft.com/keys/microsoft.asc | sudo tee /etc/apt/trusted.gpg.d/microsoft.asc

  

This command is used to download the Microsoft GPG (GNU Privacy Guard) key from a specified URL and then add it to the trusted GPG keyring on a Debian-based Linux system.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfcKmhdHp_exNZjeg-mGP4UzD6F_V-GlXUd7xFqdN-gE_-0IwSgaNWVR5RrC8ERAnY892AkH0kSQqJtzZZ0_Hc_7alo1JhW_00SSqmbo2vK2knUbefA_RDQgXNEf75ibFG61XU8fDdAiTMYun_0WECIwzgN?key=VKRitSN_Nk2iZ-d42Pg8vQ)

  
  

Step2. sudo add-apt-repository "$(wget -qO- https://packages.microsoft.com/config/ubuntu/20.04/prod.list)"

  

This command is used to add the Microsoft SQL Server repository to the list of APT (Advanced Package Tool) sources on a Ubuntu 20.04 system. 

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfk-rUnzteDD2LkHDosYj1n28c8txd-LeR6spbHV4H9AjfN3H3A7A6DoYi5tqoRWZplCqD6o7l65bJW3DRp9RmLpCSDDLCUSgrynMxS4zCLtkeMyDtb-2etmGPdcP6Nf5mPpBsJBe8LpmMXU8xruN4qIes?key=VKRitSN_Nk2iZ-d42Pg8vQ)

  

Step3. sudo apt-get update

sudo apt-get install sqlcmd

  

These commands are commonly used when setting up and configuring Microsoft SQL Server on a Linux system. sqlcmd is a command-line utility that provides a way to interact with SQL Server from the command line. It allows you to execute T-SQL queries, scripts, and commands.

  

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeZSyquyR0hXJ1IE35G0ipdiVEkf2vUkb9JrfOL5azy5zvm81X4_pyxrwkw6ONlGfE7IeK9S8-9cozCc8BQxBfCMN5dHKlF2rFOGRJ3-WmuKXbk06_bY_dD3lRSNmH8N3P2n_ER82ThlmDoz4aiqmsTUIFs?key=VKRitSN_Nk2iZ-d42Pg8vQ)

  
  
  

To execute the sqlcmd command line for the MSSQL Server, we will now use the command provided below

  

Step1.  sqlcmd -S localhost -U sa -P 'manish\_123'

  

The sqlcmd command is a command-line tool that is used to connect to and execute Transact-SQL commands on a Microsoft SQL Server database.

  

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeRJ7-YKqiVDmCr7rItFhaBnlAGiH4srzMyW709v29N0QJtuME4Jre8jCQsOsxvKLAOHKz_tAmTXXMOHQpNa3Sm-0t4gsaqvucFV3A_QVv09XbFYAI7emkkW618o51k6C354t-0P-5aNoSmJX4s1ZfUpsHN?key=VKRitSN_Nk2iZ-d42Pg8vQ)

  
  
  

Step2. select name from sys.databases;

  

The SQL query select name from sys.databases; retrieves the names of all databases from the system catalog view sys.databases.

  

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeDu_g_xmHh98eY5MAgznPMBefPZXbI7ToCY_OtDWiTGwrp07mSxexwUirHoOoj30LZufyJ-wUgmTs9iNDhBxvbmHC-4jyGbHO_TFw4Dku_T8OTfo194wkk9pZABlCUkPAFz_4se9whQRjvz3qO9qybrQo?key=VKRitSN_Nk2iZ-d42Pg8vQ)

  
  

Step3. CREATE DATABASE manishdb;

  

The SQL command CREATE DATABASE manishdb; is used to create a new database named "manishdb" in a Microsoft SQL Server environment. 

  

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcAm0UlrrqN9zzZtU4Fyn_ptZC5PLpTpihpYW7pfkhw_xsO-X6lyz8x1jy2FwF3ja9c_JKWPhDfkw6y3jzLWZUG-7_DXW2AD5i6MH-IEGvR6xmNnAQOAyv_h237nkmXxb3iIlKzkDSbACqxv_olJaw_BOlD?key=VKRitSN_Nk2iZ-d42Pg8vQ)

  

Step4. use manishdb;

  

The command use manishdb; is a SQL command used to switch or select a specific database in a database management system (DBMS).

  

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXftPGUcpSD-eVNx8L_LS8RmrtghrN1ZB-aQKa4b97LbRU-4ymKbVRvi_DCQDD6LdImAOgD9r_0ol9ZQWvGsZSvdUnutXwxVdquKXoUkSXwMNhCol8c3K9c9kFmfZJAksGLZhDv1c6LgCHbV_lv6t4mN620?key=VKRitSN_Nk2iZ-d42Pg8vQ)

  
  
  

Step5. create table mytable(id int,name varchar(100));

  

The command create table mytable(id int, name varchar(100)); is a SQL statement used to create a new table in a database.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeod9IASkBsLGImHDBztvTQTKyhE9RGiwAK6B-0SfJV3vXRhQLRHtMn_gN4RlY8SKIBefu2bOI3LrJiiEQ4hAVrDo8ta2GjwX6O4LBud9zWQiopwNPLyBBNFHiAOXwu_CHUl7dtgVaD2rAGCfNs3rUgKar5?key=VKRitSN_Nk2iZ-d42Pg8vQ)

  

Step6. select name from sys.tables;

The command select name from sys.tables; is a SQL query used to retrieve information about table names from the system tables.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfaBVxnrWsBW4qyiNzR5rrpJmtMtAS1kpOye5OKf34RfH9fwW1o0tYkVYCZSYZ2S3_XSJ-CiJ2jzd0Egc-yj9fhLlE_KUT0pEJgf9q8RcTLrAg1RNnyO0ZcvcfgUXOPNs77ASD2OiMTyx1R6jPG59vI6aLz?key=VKRitSN_Nk2iZ-d42Pg8vQ)

  

Step7. insert into mytable(id,name) values(1,'manish');

The command insert into mytable(id, name) values(1, 'manish'); is a SQL statement used to insert a new row of data into the "mytable" table.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXffB39RKmDJUGPI3mDXqeBCDi5vC3pssbiXjeADjRkfAzHnVr1rKHhLJ9M6JGB3v8Wny-4n2UlIQCkneOKgBkPzdDBFECIgd0EWlAZ-KGHHOtIhBdZiz6ElJ2y_jutsVFLqRx95_k0e1ieESQpH1sEX_yk7?key=VKRitSN_Nk2iZ-d42Pg8vQ)

  

Step8. select \* from mytable;

The command select \* from mytable; is a SQL query used to retrieve all the rows and columns from the "mytable" table.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfCNT-XY6fwlId30XMDCT3p4xcd-IHzf6rXs-E52OItOjs4iPHK2ptD3bSJvGwFuLQakitVwxB3Kl4n-HkbRejSDh-SNXzk-KYruX6v2v9K3Gm3foMdrMk4UkYzC8s70ZAiE1iDCV-IkZe6ZlSEJreQH64v?key=VKRitSN_Nk2iZ-d42Pg8vQ)

  

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfJl6l1ZYaj4lNGoY8KkaBNKulEzTmP1Dro28c-hl6OwGypAOpT-xWeLJcAM6C-GJen6b8dUWiv2f1U18O9L1xjsV-8I_ace-d1TlZ7bPzTTNC9v1EkAdDUYwKfqaXQny1kS_gyS-CA3Mvj57mV_oolDOgq?key=VKRitSN_Nk2iZ-d42Pg8vQ)

PostgreSQL is a type of database that helps store and manage information. It's like a digital filing cabinet where you can organize and retrieve data easily. PostgreSQL is known for being powerful, open-source, and able to handle large amounts of data. It's often used in applications and websites to store and organize information efficiently.

  

Below, I have set up PostgreSQL, and you can see the process.

Step1. sudo apt update

The command sudo apt update is used in Debian-based Linux distributions, such as Ubuntu, to update the local package list on your system.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfAKrWiBH4cOeE2dPlykJpgZQoarsYyp0R7jL3sPDwEH7Yicedt6QCH98fydn7jNsXX-89VCQAqZ2AjiHWZxCKL1INqFltQmmKtDMYgI5uKDriKzIo3_APFx0f2ujDG1ByQoXW1-lVvLXWgyYWgcYSjGnPu?key=VKRitSN_Nk2iZ-d42Pg8vQ)

  

Step2. sudo apt install gnupg2 wget vim

The command sudo apt install gnupg2 wget vim is used in a Debian-based Linux distribution, such as Ubuntu, to install specific software packages. 

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcgOIGHhxmRdp4SI_cnotngLSUz4CC6XWcAXNuxCZuWEDZB7f_PVPiZvRSNT7YRlZIzxNNJeB5qbBBl9n4uBHyeeNV-zdeDGTIv9W_0VknJ1Vclyv6fz7QJTMQh_kLyCu0gRC3mcvKwcsWcfFfanjrQjERE?key=VKRitSN_Nk2iZ-d42Pg8vQ)

  

Step3. sudo sh -c 'echo "deb http://apt.postgresql.org/pub/repos/apt $(lsb\_release -cs)-pgdg main" > /etc/apt/sources.list.d/pgdg.list'

This command is used to add a new software repository to the list of package sources on a Debian-based Linux distribution (like Ubuntu). 

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdNvhEk36vSMOwLZ8iHyMDwmPZ8o9Wxukk_Pwq2lcO3F4CPq99V83MGkQuV9iVxvmvbcTUcu9SIUEU9PKMhHe0osaJrCPGP11lOA05t6GqDXPF938U3drQxW5iPRb56H6-gcoVaClDV_iGLRktHaIkJEr1w?key=VKRitSN_Nk2iZ-d42Pg8vQ)

  

Step4.  curl -fsSL https://www.postgresql.org/media/keys/ACCC4CF8.asc | sudo gpg --dearmor -o /etc/apt/trusted.gpg.d/postgresql.gpg

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfzWWClJ2MMeLtBogLoj1mHDY63idmfzHE-VB5MWyIl9FnZCa_EW5ncsEWXmuK_MkqeFBchkjr8NNFXleLVtOlndMShuuj-SMHj0kWv7NvhneHdxmFEFTfy4IT-Jr4VeCZvVluZd9YsOyBIin7-tHYI8FUf?key=VKRitSN_Nk2iZ-d42Pg8vQ)

  

Step5. sudo apt update

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfhpIz5SV-ohMLYdTCFz7Uh-pngzc4KOAR7UDvl9LzK3urUiZvIwknM7xHPfnZ6_CZiozfUBPaN9haHmRH8GD3eFpyTmf08zKZMQJh3LnrutxB-jl1QAV_g4AE0pZpbm1NphHHaaDH8wLALYyWLH2fbdfFR?key=VKRitSN_Nk2iZ-d42Pg8vQ)

  

Step6. sudo apt install postgresql-16 postgresql-contrib-16

The command sudo apt install postgresql-16 postgresql-contrib-16 is used in a Debian-based Linux distribution, such as Ubuntu, to install specific versions of PostgreSQL and related contributed packages.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcvl1hVu9U8Q2w2JiHQjLdHniCnINZBdlcbAQS-Cqogq9QrthzjQOIY-ToA6VBl7sJDwPrctp-zA3s7MQxqOQzLlswtpnPgJYKfdf-r15h5z4DKlbQMRBlM7lJZKRquAICX5G2sSBNhuYAH6_Elxs8RpAgm?key=VKRitSN_Nk2iZ-d42Pg8vQ)

  
  

Step7. sudo systemctl start postgresql

The command sudo systemctl start postgresql is used to start the PostgreSQL service on a Linux system that uses the systemd init system.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcGwBtOCYyPRowrAD3s-ElFT-j5AliGDOdlaDRTAndSBvtaA-fPVsTMt5kaWjbJ_r9i7lw5EmMD_MLD7cBCP7nSBqRHtBKEyD6pUq19FQdov9vxLT7VIKjU6qBC5dCe5wSzg0Ekh7lKKLuwsVNTOlJpHpM?key=VKRitSN_Nk2iZ-d42Pg8vQ)

  

Step8. sudo systemctl enable postgresql

The command sudo systemctl enable postgresql is used to enable the automatic startup of the PostgreSQL service on boot.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeiT9t7MhYf0KuUPEZheDtBV0U8h7Oy5kww7FIM5omw19vqLLqts47CPNWFFapT9XLaIgLF0GlWoFrIGvJyVrlybfvWVVVYPXwmVhSYyNGAiz1wYJokB0vh3AlobVJhFmScOPP0Y8J_RzOXvJ0FRCMdgudm?key=VKRitSN_Nk2iZ-d42Pg8vQ)

Step9.  psql --version

The command psql --version is used to check and display the version of the PostgreSQL command-line client tool called "psql." 

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeCMcbmd_3tSHD84_nEoIrcBkCHMJlFZgV9cgb3DDFxKe7Q4CfBa7sui4rpbyydUtiv9Yum2vo8jTz7BNrOJzGx_x3jr_QdesSRuEtbiHyL3LK8vjJ66dZoLwiqeZ9-M1V3ChLTA5Wp4F2Rl1PxjV57556S?key=VKRitSN_Nk2iZ-d42Pg8vQ)

Step10. sudo vim /etc/postgresql/16/main/postgresql.conf

listen\_addresses = '\*'

The command sudo vim /etc/postgresql/16/main/postgresql.conf is used to edit the configuration file for a specific instance of PostgreSQL. 

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcpsx74uKc0GLaiqZLXT3ECgpMRebiGFPk7r8Z9LqisnfwOCfkt_CSZSFUjBYQeTG5ty0w_yhs-hUPyYYpwR8HG2YXU9UYO16mxrIR95hWxgAWHaQbVB7fOz4NCjYdGPwn-A_9aQb0dJFx_071cXJmtG5M?key=VKRitSN_Nk2iZ-d42Pg8vQ)

  

Step11. sudo sed -i '/^host/s/ident/md5/' /etc/postgresql/16/main/pg\_hba.conf

The command sudo sed -i '/^host/s/ident/md5/' /etc/postgresql/16/main/pg\_hba.conf is a sed command used to modify the authentication configuration in the PostgreSQL pg\_hba.conf file. 

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdMQ3JtCeU4ck2kdEeuUmUtR_4v6noppQI0miTB6OVUd6rt0Gp0EHk65mRqod4tSjzMfeict8dYTiQSAh78wphioxOIlFb3IcaT-KiyQQw_f4jqci6k0UfOh5j_GW7nAJuLko7KCUmhZE4s-wtrAaZSXXI?key=VKRitSN_Nk2iZ-d42Pg8vQ)

  
  

Step12. sudo sed -i '/^local/s/peer/trust/' /etc/postgresql/16/main/pg\_hba.conf

The command sudo sed -i '/^local/s/peer/trust/' /etc/postgresql/16/main/pg\_hba.conf is a sed command used to modify the local authentication configuration in the PostgreSQL pg\_hba.conf file.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcbimKEmyPqsufXEj-t8xHZMVlVpdhjpYvePyO00EIybP9kbJ2TtXaD1HHal4a6532Y4hIR1D5i9cpNBjXLNEDqiMyCuHMlWievJZWo3MQPOZA2NIlMpAIu2J_vu6keNl5E6hDqz-kzcgkGkIemMik2fVUx?key=VKRitSN_Nk2iZ-d42Pg8vQ)

  

Step13.  echo "host all all 0.0.0.0/0 md5" | sudo tee -a /etc/postgresql/16/main/pg\_hba.conf

The command echo "host all all 0.0.0.0/0 md5" | sudo tee -a /etc/postgresql/16/main/pg\_hba.conf is used to append a new line to the PostgreSQL Host-Based Authentication (HBA) configuration file, allowing connections from any IP address.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXceraTTvrI_ExU_anGiklSql2Ms39YXv06q297MS1FpqXCCxIAqI2TZIqVzKii_jqxUNPbXpROt3F4i1v-bcB-YSvinDoXlbq1tPrRQKgs8z71CZCvpV25qJksMSnT2rA_zi4DEeBuTOp6pw04ceI_I37E?key=VKRitSN_Nk2iZ-d42Pg8vQ)

Step14. sudo systemctl restart postgresql

The command sudo systemctl restart postgresql is used to restart the PostgreSQL service on a Linux system that uses the systemd init system. 

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeRCBRWV7tWa59vhaUe-2TDzkh0CUEfnDoQ3J68eIqikHBJv6e1uxXWuAO1-b0uHiK0fW8feOaBnNnMc5M3fHwvf4DbJd0e7YytQxzhzyK56ZKb9cfstMGmqKxNIfa4uV3UVYvZ8cgdGXw1rt34lmGXYyOQ?key=VKRitSN_Nk2iZ-d42Pg8vQ)

Step15. sudo ufw allow 5432/tcp

The command sudo ufw allow 5432/tcp is used to configure the Uncomplicated Firewall (UFW) to allow incoming traffic on port 5432 using the TCP protocol.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcc-yHvi7KrG3JmmuMjlsWuGbt_H3DFgMHEzewmoiKaw11X2-7LYjHBNGfEaqP-6r80lR5z0Qy8GgheWFKN-RlsTrdr0x22uDf9XYYqxpkZWsOnt7CN2UcDO4V-0Fq2KabiWOh8to2Oa0qyq2Xf-K5VbEDk?key=VKRitSN_Nk2iZ-d42Pg8vQ)

  

Step16. sudo -u postgres psql

The command sudo -u postgres psql is used to run the PostgreSQL command-line interface (psql) as the PostgreSQL superuser, typically named "postgres."

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdJjrM2qPC46q9OCOWoxzYS__EH4IaMaBzruCgyR5jr72zd2feSRf-ZQTiCucKsAo_beWmQe557ErN9nbezbhu3dmwDsHlgPSWwgkjFW4Cyd_RoRZL67sfmmCTalaLnz3RVbPjbZS4Wac6E3-Txv5xX9iVG?key=VKRitSN_Nk2iZ-d42Pg8vQ)

Step17. postgres=# \\l

The query \\l is a command specific to the PostgreSQL command-line interface (psql) and is used to list all the available databases on the PostgreSQL server. 

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcvebuvDXka0Ba2Rd_OmYMzXAb2HH2RD_9VEFI1EqhwWRecK6iW_tyo7542qkgKZiYfJKNX7fsbAEgBlBjXy14V2ZPbBpCKpFyDTkDdg7i90t-R-01R-ovpzPakj3kOvKJVNtJ7g-DPs_38G3l1Eb265jdR?key=VKRitSN_Nk2iZ-d42Pg8vQ)

  

Step18. postgres=# create database manishdb;

The query create database manishdb; is a SQL command used to create a new database named "manishdb" in a PostgreSQL database server.

  

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXe-M9ka7EkT6iF9yKKRKsBJ-Hs3hcfXT3iC8ZAZq4mUvsmTj0wRp7Yyw504rAvzBe_FV8ln9nJ70lmKbrv6ugqAehZyRGjFdHK0xzKkZnAtfmHSNyValUtDF723dTdq8zU-UpPMTpmjOO61k91Oy4jBwkIn?key=VKRitSN_Nk2iZ-d42Pg8vQ)

  
  
  

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcWw3Mbd0Qmd98otHCFgFsQlYYaB08iQKT15BEeicVHTPnRSHHTfLArP243AzDKiFyH6EIvc5_dup1BthQWGfE89xN-AMaX8M3bGu80fcqeQ-xULWCUsdAMA1EHwqSBZIeJUxTQwpGTCwGTXBZrpAS-cpWt?key=VKRitSN_Nk2iZ-d42Pg8vQ)

The pgloader tool has been used for migrating a database from Microsoft SQL Server to PostgreSQL.

pgloader is a powerful and flexible data migration tool used for loading data from various sources into PostgreSQL databases. It supports the transformation of data types, mapping between source and destination columns, and handling differences in database schemas. pgloader is particularly useful for efficiently transferring data between different database systems or versions while taking care of the necessary adjustments to ensure compatibility.

  

Step1. sudo apt-get install pgloader

The command sudo apt-get install pgloader is used on Debian-based Linux distributions, such as Ubuntu, to install the pgloader tool. 

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfDaNU9ZRugp5y6SFoiXBeCmfFg0N_p5F5hXC7YoJ4fCN7e_y5x2twApZ9E2M03TyrgtU90lAEIgKFcsf83SxMaj-iMcBNUvm4XIFfPFp2PuHodQ1SQ1DuOMVzO8z14dODeyv81I9C3Lk4SyPH8RN_VzxLY?key=VKRitSN_Nk2iZ-d42Pg8vQ)

  

Step2. pgloader "mssql://SA:Manish\_123@192.168.122.168:1433/manishdb" "postgresql://postgres:manish\_123@192.168.122.168:5432/manishdb"

This pgloader command connects to the MSSQL server, reads data from the specified source database (manishdb), and then loads that data into the PostgreSQL server, creating or updating the destination database (manishdb).

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeJDEiVF0m79C-B0aX7hVWiu_C1t7YFGYGTNTtH1QNAkG8LBD4h6l_RIESKkbxfE3hp3c9BkpQKZJ-ucBXaqLLZ-YrGTy3E4-6IiliJNAYf3iByhvCS_GHQa8AH2YWQUJ48f0U1lm_WPNkt3J-y4xRuw2ff?key=VKRitSN_Nk2iZ-d42Pg8vQ)

  
  

After running the pgloader command, we will connect to the PostgreSQL database, specifically to the 'manishdb' database. We will then inspect the 'dbo' schema to verify whether the data from the 'mytable' in the source database has been successfully migrated.

Step1. postgres=# \\c manishdb;

The command \\c manishdb; is used in the PostgreSQL command-line interface (psql) to connect to a specific database named "manishdb.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcjlHL1dxKl26vClvNxeWIeNgcVDm2F84PHZRHWpMMAHD9mJ3uKb6PWoiWY98xjVzEMFb25v0DZF4ZfCzCLsU-1aC-ZgNzCyRox6JrbmEdo3h6v8QnRxElX2xnlFcxs09UpL8QHWIrYLmHuER2iByfB8ySZ?key=VKRitSN_Nk2iZ-d42Pg8vQ)

  

Step2. manishdb=# \\dn

The command \\dn is used in the PostgreSQL command-line interface (psql) to list all available schemas in the currently connected database.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeYI7yDGTXVxrtPjtZyzGAGmynL6Sle5GVpDERfDS5UD_6-yQwUaSiHtG5MDhySt6DVu6XMSzN5QAkXTj_3EOMojXw-Y1Hgz163PQC6WKdYvSl_SbnzJa1pTf6j98zROToz9xqFNyR_uB4-qfdSxhAdnZQJ?key=VKRitSN_Nk2iZ-d42Pg8vQ)

Step3. manishdb=# select \* from dbo.mytable;

The command select \* from dbo.mytable; is a SQL query executed in the PostgreSQL database.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdUHvdDFO91BtkdJdpXAAsWsgbq7RAbxqqNilzT688c7nmNUCiqD9vzuR88knxSrbsnMsYTQrIloulQSkvhjmjdQE5KGKWMa7wQevbHG0Dn1H8uY08D4143CBqs5b15g5Pwvnh_tMBkjjELDGuZaaptgjW_?key=VKRitSN_Nk2iZ-d42Pg8vQ)

  

The table has been successfully migrated from Microsoft SQL Server to PostgreSQL.

  
  
  
  
  
  
  
  
  
  
  
  
  
  
  

*   After setting up Microsoft SQL Server and PostgreSQL containers using Podman, I have migrated a database from Microsoft SQL Server to PostgreSQL using pgloader. You can see the steps below.
    

  

Step1.  podman run --name postgres-container -e POSTGRES\_PASSWORD=manish\_123 -p 5433:5432 -d docker.io/library/postgres

This command is creating and running a PostgreSQL container named "postgres-container", setting the password for the PostgreSQL user, mapping the port, and running it in the background.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXd_QTASFkFdrMsy02_rKqBphdkCGNrVIrqoqvvPh01YMDg8SS5Q8gBbBxM4uddNJcMqtGORyoKY1ZQNfxHYV8OP-eu1jLP2U0EuWqoMwUA9-9dpnycsEuIQEfQ3IXCZS1QDL60CnuLTYPXChi693YRZOqg?key=VKRitSN_Nk2iZ-d42Pg8vQ)

Step2. podman run --name sql-server-container -e ACCEPT\_EULA=Y -e SA\_PASSWORD=Manish\_123 -p 1433:1433 -d mcr.microsoft.com/mssql/server

This command creates and runs a Microsoft SQL Server container named "sql-server-container", accepting the EULA, setting the SA password, mapping the port, and running it in the background. This allows you to access and interact with the SQL Server instance within the container

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdR0Xj-bcMZCq_zOWgPBF33NGGaQM8LK5O1Ym2nOsavXqui10ZdC1SmMgPoIT2nN4ZW8o7jxXmyGS9iIMTPxAt9v7u7juQNXmIhpRpdviFzh0vB4F8C423W06UeLx3fm9Mvr6BJBvXe5-XpFWt3m_h-peaj?key=VKRitSN_Nk2iZ-d42Pg8vQ)

  

Step3. podman exec -it f237055e1aa7 /bin/bash

The podman exec command is used to execute a command inside a running container.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfPsx19AR-PTFQq10-3B4GjT0upYqaexXRr3am_mnhg0yiafa3ElpFPjY17iJ_3rmLdwLwkWwRKvesOADR1GQH4FqAzZW-p7Q6uZu0dDfcCZfGL1uH_MKUA8I9nSZki4YlCDI_spgzncLjmYNeXtcDPxf0?key=VKRitSN_Nk2iZ-d42Pg8vQ)

  

Step4. /opt/mssql-tools/bin/sqlcmd -S localhost,1433 -U sa -P Manish\_123

The sqlcmd command is a command-line tool provided by Microsoft for interacting with SQL Server

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfQU2ZPOBc769uJep6L6OwMbmYcWEL0BDtcj-HP7KAw-WNGxOUJujh0ZJL03Lesk1QW1PBlCP8Ltf0ib5hoU29xJX0stIOsYeKGTln_Zeb4dyRsgMUncvUg8rKJW_nKCntXtOqCxp3QVtY2OaoY6SDwDlc?key=VKRitSN_Nk2iZ-d42Pg8vQ) 

Step5. CREATE DATABASE manishdb;

  

The SQL command CREATE DATABASE manishdb; is used to create a new database named "manishdb" in a Microsoft SQL Server environment. 

  

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcAm0UlrrqN9zzZtU4Fyn_ptZC5PLpTpihpYW7pfkhw_xsO-X6lyz8x1jy2FwF3ja9c_JKWPhDfkw6y3jzLWZUG-7_DXW2AD5i6MH-IEGvR6xmNnAQOAyv_h237nkmXxb3iIlKzkDSbACqxv_olJaw_BOlD?key=VKRitSN_Nk2iZ-d42Pg8vQ)

  

Step6. use manishdb;

The command use manishdb; is a SQL command used to switch or select a specific database in a database management system (DBMS).

  

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXftPGUcpSD-eVNx8L_LS8RmrtghrN1ZB-aQKa4b97LbRU-4ymKbVRvi_DCQDD6LdImAOgD9r_0ol9ZQWvGsZSvdUnutXwxVdquKXoUkSXwMNhCol8c3K9c9kFmfZJAksGLZhDv1c6LgCHbV_lv6t4mN620?key=VKRitSN_Nk2iZ-d42Pg8vQ)

  
  
  

Step7. create table mytable(id int,name varchar(100));

  

The command create table mytable(id int, name varchar(100)); is a SQL statement used to create a new table in a database.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeod9IASkBsLGImHDBztvTQTKyhE9RGiwAK6B-0SfJV3vXRhQLRHtMn_gN4RlY8SKIBefu2bOI3LrJiiEQ4hAVrDo8ta2GjwX6O4LBud9zWQiopwNPLyBBNFHiAOXwu_CHUl7dtgVaD2rAGCfNs3rUgKar5?key=VKRitSN_Nk2iZ-d42Pg8vQ)

  

Step7. select name from sys.tables;

The command select name from sys.tables; is a SQL query used to retrieve information about table names from the system tables.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfaBVxnrWsBW4qyiNzR5rrpJmtMtAS1kpOye5OKf34RfH9fwW1o0tYkVYCZSYZ2S3_XSJ-CiJ2jzd0Egc-yj9fhLlE_KUT0pEJgf9q8RcTLrAg1RNnyO0ZcvcfgUXOPNs77ASD2OiMTyx1R6jPG59vI6aLz?key=VKRitSN_Nk2iZ-d42Pg8vQ)

  

Step8. insert into mytable(id,name) values(1,'manish');

The command insert into mytable(id, name) values(1, 'manish'); is a SQL statement used to insert a new row of data into the "mytable" table.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXffB39RKmDJUGPI3mDXqeBCDi5vC3pssbiXjeADjRkfAzHnVr1rKHhLJ9M6JGB3v8Wny-4n2UlIQCkneOKgBkPzdDBFECIgd0EWlAZ-KGHHOtIhBdZiz6ElJ2y_jutsVFLqRx95_k0e1ieESQpH1sEX_yk7?key=VKRitSN_Nk2iZ-d42Pg8vQ)

  

Step9. select \* from mytable;

   Step10:to set password in db:    \\password postgres

The command select \* from mytable; is a SQL query used to retrieve all the rows and columns from the "mytable" table.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfCNT-XY6fwlId30XMDCT3p4xcd-IHzf6rXs-E52OItOjs4iPHK2ptD3bSJvGwFuLQakitVwxB3Kl4n-HkbRejSDh-SNXzk-KYruX6v2v9K3Gm3foMdrMk4UkYzC8s70ZAiE1iDCV-IkZe6ZlSEJreQH64v?key=VKRitSN_Nk2iZ-d42Pg8vQ)

  

Step10. podman exec -it postgres-container psql -U postgres

After running this command, you should be within the PostgreSQL command-line interface (psql) and able to interact with the PostgreSQL database running inside the "postgres-container

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfzFWWG2hD6itEBfoUDW8RwqLI8h34h7NgeVNjRUullYwvUhpNp_0VN76gatAEMH9eiWttyi487dl3vXNomXwLt2iCQSzXEJ5G-g_BgbKkhYny-d9utJG44cgg96-wMmR2L7d9Y2xRgqQQrBxV6ONMc704?key=VKRitSN_Nk2iZ-d42Pg8vQ)

Step11. postgres=# \\l

The query \\l is a command specific to the PostgreSQL command-line interface (psql) and is used to list all the available databases on the PostgreSQL server. 

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcvebuvDXka0Ba2Rd_OmYMzXAb2HH2RD_9VEFI1EqhwWRecK6iW_tyo7542qkgKZiYfJKNX7fsbAEgBlBjXy14V2ZPbBpCKpFyDTkDdg7i90t-R-01R-ovpzPakj3kOvKJVNtJ7g-DPs_38G3l1Eb265jdR?key=VKRitSN_Nk2iZ-d42Pg8vQ)

  

Step12. postgres=# create database manishdb;

The query create database manishdb; is a SQL command used to create a new database named "manishdb" in a PostgreSQL database server.

  

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXe-M9ka7EkT6iF9yKKRKsBJ-Hs3hcfXT3iC8ZAZq4mUvsmTj0wRp7Yyw504rAvzBe_FV8ln9nJ70lmKbrv6ugqAehZyRGjFdHK0xzKkZnAtfmHSNyValUtDF723dTdq8zU-UpPMTpmjOO61k91Oy4jBwkIn?key=VKRitSN_Nk2iZ-d42Pg8vQ)

  

Step13. pgloader "mssql://SA:Manish\_123@192.168.122.168:1433/manishdb" "postgresql://postgres:manish\_123@192.168.122.168:5432/manishdb"

This pgloader command connects to the MSSQL server, reads data from the specified source database (manishdb), and then loads that data into the PostgreSQL server, creating or updating the destination database (manishdb).

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXf-YjpRLxH9P1JQlst4Yeac9uh0Bx7_Mqriybmlu0YUI6YoLEwAeWZoF0W9wmwHWCYis_aFZGerqEE03-IYD4UeqQNgUiz2GeHK8E24EC2ikH5-If1p2E9rJIam_5nxGrAM27AGFEFVwO9aeDpFHeIj_lP4?key=VKRitSN_Nk2iZ-d42Pg8vQ)

After running the pgloader command, we will connect to the PostgreSQL database, specifically to the 'manishdb' database. We will then inspect the 'dbo' schema to verify whether the data from the 'mytable' in the source database has been successfully migrated.

Step1. postgres=# \\c manishdb;

The command \\c manishdb; is used in the PostgreSQL command-line interface (psql) to connect to a specific database named "manishdb.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcjlHL1dxKl26vClvNxeWIeNgcVDm2F84PHZRHWpMMAHD9mJ3uKb6PWoiWY98xjVzEMFb25v0DZF4ZfCzCLsU-1aC-ZgNzCyRox6JrbmEdo3h6v8QnRxElX2xnlFcxs09UpL8QHWIrYLmHuER2iByfB8ySZ?key=VKRitSN_Nk2iZ-d42Pg8vQ)

  

Step2. manishdb=# \\dn

The command \\dn is used in the PostgreSQL command-line interface (psql) to list all available schemas in the currently connected database.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeYI7yDGTXVxrtPjtZyzGAGmynL6Sle5GVpDERfDS5UD_6-yQwUaSiHtG5MDhySt6DVu6XMSzN5QAkXTj_3EOMojXw-Y1Hgz163PQC6WKdYvSl_SbnzJa1pTf6j98zROToz9xqFNyR_uB4-qfdSxhAdnZQJ?key=VKRitSN_Nk2iZ-d42Pg8vQ)

Step3. manishdb=# select \* from dbo.mytable;

The command select \* from dbo.mytable; is a SQL query executed in the PostgreSQL database.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdUHvdDFO91BtkdJdpXAAsWsgbq7RAbxqqNilzT688c7nmNUCiqD9vzuR88knxSrbsnMsYTQrIloulQSkvhjmjdQE5KGKWMa7wQevbHG0Dn1H8uY08D4143CBqs5b15g5Pwvnh_tMBkjjELDGuZaaptgjW_?key=VKRitSN_Nk2iZ-d42Pg8vQ)

  

The table has been successfully migrated from Microsoft SQL Server to PostgreSQL.