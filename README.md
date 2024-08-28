# Flaxor
# **Online Gender-Based Violence (OGBV) Detection in African Contexts**

## **Main Objective**

The primary goal of this project is to create a comprehensive repository of Online Gender-Based Violence (OGBV) lexicons tailored to African languages and contexts. This repository will significantly enhance the detection and understanding of online violence across various platforms, ensuring that the nuances of African languages and cultures are adequately addressed.

## **Implementation Method**

This project employs an AI-based lexicon generation and update system to dynamically create and refine a lexicon for OGBV detection. The system is designed to evolve with emerging trends in language use, ensuring that the lexicon remains relevant and effective in identifying instances of online gender-based violence.

## **Project Structure**

### **1. OGBV Scraper**

The `ogbv_scraper` directory houses a web scraper built using the Scrapy framework. This tool is designed to scrape content from websites, particularly those relevant to African contexts, such as local news sites, blogs, and social media platforms. The scraped data is then analyzed to identify potential instances of OGBV.

- **Main Scraper Script**: `ogbv_scraper/ogbv_scraper/spiders/ogbv_spider.py`
  - **Usage**: Specify the target website within the spider script and run the command:  
    ```bash
    scrapy crawl ogbv
    ```
  - **Output**: The scraper generates a file containing the scraped data, which is saved one directory back for further analysis.

- **Analysis Script**: After scraping, use the following command to analyze the data:
  ```bash
  python gpt_analysis.py
  ```
  This script processes the data, identifying sentences that may exhibit gender-based violence. The output is another JSON file that categorizes the nature of each sentence.

  **Note**: This scraper is optimized for African websites, posts, and blogs to ensure cultural relevance and accuracy in detection.

### **2. OGBV Monitoring**

The `ogbv_monitoring` directory contains a Django project that monitors social media platforms (Instagram, X, Facebook) for OGBV. This tool leverages the Django templating engine to track and analyze conversations in real-time, focusing on the detection of OGBV-related content.

- **Key Features**:
  - **Social Media Monitoring**: Tracks conversations on Instagram, X (formerly Twitter), and Facebook.
  - **Analysis Tools**: Uses AI and hashtag analysis to identify and classify OGBV-related content.
  - **Customizable Monitoring**: Adjust the monitoring parameters to target specific conversations or user groups.

- **API Access Keys**:
  To successfully use the monitoring tool, you'll need API access keys from the respective social media platforms. Please ensure that you obtain the correct keys, such as the Facebook user key, which is crucial for proper data access.

  **Tip**: Visit the developer portals of Instagram, X, and Facebook to request and manage your API keys. Ensure that you follow the specific instructions provided by each platform.

## **Setting Up the Project**

1. **Create a Virtual Environment**:  
   To ensure that your project dependencies are isolated, create a virtual environment:
   ```bash
   python -m venv venv
   ```

2. **Activate the Virtual Environment**:  
   On Windows, navigate to the Scripts directory and activate the environment:
   ```bash
   cd venv/Scripts
   ./activate
   ```
   Then, return to the root folder:
   ```bash
   cd ../..
   ```

3. **Install Required Dependencies**:  
   Once the virtual environment is active, install the required Python packages by running:
   ```bash
   pip install -r requirements.txt
   ```

## **Contributing**

We welcome contributions to this project, particularly those that enhance the lexicon's accuracy and cultural relevance. Whether you're an AI enthusiast, a linguist, or simply passionate about combating online gender-based violence, your input can make a significant impact.
