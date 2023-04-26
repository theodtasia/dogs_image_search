**Content-Based Dog Image Retrieval**
This project is a straightforward implementation of a content-based image retrieval engine that utilizes Python for the application logic and PostgreSQL as a storage backend. The VGG16 model is employed to extract features from images.

**Dataset**
The original Oxford-IIIT Pet Dataset, which comprises approximately 7000 dog and cat images annotated with their corresponding breeds, can be found at the link provided.

**Requirements**
To use this project, you must create a Python virtual environment and install the packages found in the base_requirements.txt file.

To create and activate a Python virtual environment using Anaconda:

`conda create --name image_search_engine env python=3.8
conda activate image_search_engine`

To install the necessary base Python packages:

`pip install -r requirements.txt`

**PostgreSQL:**
To use this application, you must establish a connection with a PostgreSQL database and create a table named pet_images. To establish a connection with PostgreSQL, create a .env file in the following format:

`
DB_HOST=localhost
DB_PORT=5432
DB_NAME=image_search
DB_USER=postgres
DB_SECRET=mpompos`

**Setting up the Dataset of Images:**

Go to the following link: http://vision.stanford.edu/aditya86/ImageNetDogs/

Scroll down and click on the "Download images" link.

This will download a file named "images.tar" to your computer.

Extract the contents of the tar file using a file archiver program such as 7-Zip or WinZip. This will create a folder named "Images" containing the dataset.

Add the folder inside the dog_images directory of the project

**Setting up the PostgreSQL Database:**

Run the following command to create the dog_images table:

`python db.py --do=create`

Run the following command to add the dog images records into to the table of the PostgreSQL database. 

`python db.py --do=add`
