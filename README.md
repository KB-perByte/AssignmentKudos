Scrapping data out of EPFO and MCA

How to get started! 
    - pip3 install -r requirements.txt 
    OR
    - pip install -r requirements.txt
    
    This is wierd, but needed to solve the capthas
    - https://medium.com/@ahmetxgenc/how-to-use-tesseract-on-windows-fe9d2a9ba5c6
    - Once, Teseract OCR is installed there needs to be a path specification in the code 
    - statics\captcha_reader.py -> line 86 -> replace the path of tesseract.exe incase it is different

    On this level just execute the command listed below to get the API server started
    - [AssignmentKudos\AssignmentKudos> uvicorn main:app --reload]
    -  uvicorn main:app --reload
    
    Move to the server URL
    - http://127.0.0.1:8000/docs
    - docs coz, it will give swaggerUI to play with the APIs 

    API specs
    for EPFO data [captcha based]
        NOTE - there are CAPTCHA retries as OCR reads some captcha wrong, so API might be slow but working :)
        - http://127.0.0.1:8000/epfo/flipkart 
        - curl -X GET "http://127.0.0.1:8000/epfo/flipkart" -H  "accept: application/json"
    for MAC data [no captcha]
        - http://127.0.0.1:8000/mca/flipkart
        - curl -X GET "http://127.0.0.1:8000/mca/flipkart" -H  "accept: application/json"
    for dev info
        - curl -X GET "http://127.0.0.1:8000/devInfo/" -H  "accept: application/json"


