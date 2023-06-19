# US-visa-appointment-notifier

This is just a script I put together to check and notify me via email ([SendGrid](https://sendgrid.com/)) when there's an earlier date before my initial appointment date. It doesn't handle **rescheduling**.

## How it works

* Logs you into the portal
* checks for schedules by day
* If there's a date before your initial appointment, it notifies you via email
* If no dates found, the process waits for set amount of seconds to cool down before restarting and will stop when it reaches the set max retries.

> see `config.js` or `.env.example` for values you can configure

## Configuration

copy the example configuration file exampe in `.env.example`, rename the copied version to `.env` and replace the values.

### SendGrid config values

You can create a free account with https://www.sendgrid.com/ which should be sufficient and use the provided sandbox domain on your dashboard. The `SENDGRID_API_KEY` can be found in your SendGrid settings, it starts with `SG.xxxxxx`. You'll need to add authorised sending email.


## FAQ

* How do I get my facility ID - https://github.com/theoomoregbee/US-visa-appointment-notifier/issues/3
* How do I get my schedule ID - https://github.com/theoomoregbee/US-visa-appointment-notifier/issues/8, https://github.com/theoomoregbee/US-visa-appointment-notifier/issues/7#issuecomment-1372565292
* How to setup Mailgun Authorised recipients - https://github.com/theoomoregbee/US-visa-appointment-notifier/issues/5

## How to use it

* clone the repo
* run `npm i` within the cloned repo directory
* start the process with `npm start`
