# Submit-Testing
A server to use to test submit plugins. If you run the Manifest_creation.py file it will generate the correct manifest for testing a submit plugin for any files put in the public folder. If you run the app (using the install instructions below) the app will return files at the urls generated by the Manifest_creation.py script. Note that if running the the server using docker line 10 of Manifest_creation.py must be changed from `host_address = "http://localhost:5000/public/"` to `host_address = "http://localhost:3001/public/"`.

# Install
## Using docker
Run `docker run --publish 3001:5000 --detach --name submit-testing synbiohub/submit-testing:snapshot`
Check it is up using localhost:3001.

## Using Python
Run `pip install -r requirements.txt` to install the requirements. Then run `FLASK_APP=app python -m flask run`. A flask module will run at localhost:5000/.