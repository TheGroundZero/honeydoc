HoneyDoc creates a "honey" document including things like fake names and social security numbers to look appealing to would be attackers. It also includes a 1x1 pixel png file called hello.png as the tracking image so that you can see the IPs of who opens the document in your web server logs. To install the image, place it in your web servers root directory (or any other directory you want to use) and specify your URL using the --url flag when generating the document. 

Once the document is generated it can be edited and personalized to make it look any way you want.

usage: `HoneyDoc.py [-h] [-t TITLE] [-c COUNT] [-b] [-u URL] [-e EXT]`

Optional arguments:

    -h, --help                Show this help message and exit
    -t TITLE, --title TITLE   Specify a custom document title.
                              Default is Employee Information
    -c COUNT, --count COUNT   Number of fake records to create.
                              Default is 10
    -b, --beacon              Include a beacon image.
    -u URL, --url URL         Set a custom URL for the beacon image.
                              Default is http://127.0.0.1/hello.png
    -e EXT, --ext EXT         File extension.
                              Default is doc

Example of how to set a custom document title and image:
`python.exe HoneyDoc.py -t "MyCompany Employee Info" -c 20 -b -u http://www.mysite.com/image.jpg`
