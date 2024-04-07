# Mongodb

```js

const { MongoClient } = require("mongodb");

async function main(){
    const uri = "mongodb://127.0.0.1:27017";

    const client = new MongoClient(uri);
    const myDB = client.db("projects");
    const myColl = myDB.collection("todos");
    console.log(myDB)
    const doc = { 
      "todo": {
        "title": "Clean bathroon"
      }
    };
    const result = await myColl.insertOne(doc);
    console.log(`A document was inserted with the _id: ${result.insertedId}`,);

    try{
        await client.connect();
        await listDatabases(client);
    } catch (e){
        console.error(e);
    } finally {
        await client.close();
    }
}
main().catch(console.error);

async function listDatabases(client) {
    databasesList = await client.db().admin().listDatabases();
                    

    console.log("Databases:");
    databasesList.databases.forEach(db => {console.log(` - ${db.name}`)});

};

```
