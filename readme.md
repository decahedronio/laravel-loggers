# Laravel Logging Tools for L5.6+

We've collected some of our favorite logger configurations and packaged them up
for you. 

## Available Channels

- `DatabaseCounter` maintains a counter for how often each event occurs by unique log messages.
It also contains the first and last occurrence.
- `RedisCounter` is a simpler (and more lightweight) counter. It also counts by unique
message, but only maintains the 
- `EloquentModel` writes a new Eloquent model for each log event. This can get hefty,
 so we recommend using this only for important events. Handy if you want to read and display
 log information in your app UI. Should not actually perform any inserts until the logger is closed,
 at which point it does a mass insert.
 - `LaravelMailer` sends emails using Laravel's built-in mailer.
 
## Processors

- `ComposerVersionProcessor` adds version information from each package loaded in your composer.json.