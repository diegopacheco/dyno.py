## dyno.py

This is a simple dyno like driver implementation in Python for Dynomite(https://github.com/Netflix/dynomite).

## Features

* Connection Management
* Fallback and Retrys

## Usage
```python
def simpleCode(r):
    result = r.get('foo')
    print result

def main():
    driver = DynoPythonDriver('127.0.0.1|127.0.0.1|127.0.0.1')
    while(True):
        try:
            driver.runWithFallback(simpleCode)
            time.sleep(1)
        except Exception as e:
            print "Abording program... Error: " + str(e)
            break
main()
```

## Related Projects

* Dynomite-Docker: Docker images to run dynomite in your local machine. https://github.com/diegopacheco/dynomite-docker
* DCC: Java utility to check is deynomite cluster is healthy and working fine https://github.com/diegopacheco/dynomite-docker
