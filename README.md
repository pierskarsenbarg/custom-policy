# Custom policy packs

We have four folders:

1. policy-packs - this contains the custom default policy packs that can be shared via NPM
2. policy - this is the folder containing the actual policy as code tooling - this is where the policy as code is run from (contains `PulumiPolicy.yaml` file)
3. program - this is the Pulumi program that we'll be running
4. auto-code - this is the automation api code that we'll use to run the pulumi program alongside the policy packs

To run everything, make sure `npm install` is run in all folders:

`cd auto-code && npm install && cd ../policy && npm install && cd ../policy-packs && npm install && cd ../program && npm install`

Change to auto-code and run the following:

`npm run start`

We should see the update fail because the bucket acl is set to `public-read`