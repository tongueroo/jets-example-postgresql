# Jets Example Project with Postgresql Database Adapter

[![BoltOps Badge](https://img.boltops.com/boltops/badges/boltops-badge.png)](https://www.boltops.com)

This project was generated with:

    jets new demo --database postgresql
    cd demo
    jets generate scaffold Post title:string

Then the demo controller was added and connected to the `/info` route.

* [config/routes.rb](config/routes.rb)
* [app/controllers/demo_controller.rb](app/controllers/demo_controller.rb)
* [app/views/demos/index.html.erb](app/views/demos/index.html.erb)

The info route shows database info.

## Deploy

Configure a `.env` file to use the actually DATABASE_URL. Example:

    DATABASE_URL=postgresql://USERNAME:PASSWORD@DNS-HOSTNAME.us-west-2.rds.amazonaws.com/DBNAME?pool=5

You can use `.env`, `.env.remote`, `.env.development.remote`, etc per [Env Files](http://rubyonjets.com/docs/env-files/)

Then you will be ready to deploy:

    jets deploy

If you visit the `/info` path, you'll should see something like this:

![](https://raw.githubusercontent.com/tongueroo/jets-example-postgresql/master/screenshots/api-gateway-postgresql-info.png)
