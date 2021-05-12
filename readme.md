== Prerequisites

To run this prebuilt project, you will need:

- Couchbase 7 Installed (*With `user_profile` bucket and `profile` collection)
- NodeJS & NPM
- A Code Editor
- cURL

*After installation of Couchbase 7, and if it is running on localhost (http://127.0.0.1:8091) we can create a bucket named `user_profile` and a collection named `profile` using two curl commands that uses the Couchbase REST API:

*Create Bucket First:*

```sh
curl -v -X POST http://127.0.0.1:8091/pools/default/buckets \
-u Administrator:password \
-d name=user_profile \
-d ramQuotaMB=256
```

*Then Create Collection:*

```sh
curl http://127.0.0.1:8091/pools/default/buckets/user_profile/collections/_default \
-u Administrator:password -X POST \
-d name=profile
```

If you would like to enable testing, you can run the same commands replacing `user_profile` with `test_profile`.

Once the database and the bucket(s) are set up you can run the development environment or the test environment.


Once the repo is cloned, run `npm install` and then choose your adventure:

## Running The Application

```sh
npm start
```

## Running The Tests

```sh
npm test
```
