# br-freeport
## How to use

```
import findAvailablePort from 'br-freeport/src/index.mjs'
import http from 'node:http'
const server = http.createServer((req,res)=>{
    console.log("req recived")
    res.end("Hello World")
})

const desiredPort = process.env.PORT ?? 3000

findAvailablePort(desiredPort).then(port =>{
    server.listen(port,()=>{
        console.log(`Server is running on port http://localhost:${port}`)
    })
})
```
