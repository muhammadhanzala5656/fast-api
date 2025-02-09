#### create
python -m venv enviornmentname

#### activate
enviornmentname\Scripts\activate.ps1   

#### install packages:
pip install uvicorn
pip install fastapi

#### Check Installed Packages
pip freeze

#### Create a file called learn.py and paste this code
<pre>
  
from fastapi import FastAPI

# Create an instance of the FastAPI class
app = FastAPI()

# Define a root route
@app.get("/")
async def read_root():
    return {"message": "hello, world!"}

if __name__ == "__main__":
    import uvicorn
    uvicorn.run(app, host="127.0.0.1", port=8000)
</pre>

#### Running fastapi server

uvicorn learn:app --reload

Remember learn is the name of fastapi app file
