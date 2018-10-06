# Logging

## Configuring Logging

By default, logs are sent to the `stderr` filehandle in the terminal. However, there may be times you wish to store logs in a file.

### Sending Logs to a File

Prior to Gophish version 0.8.0, you can redirect logs from the terminal into a file using standard shell redirection:

```text
$ ./gophish > gophish.log 2>&1
```

The downside to this is that logs will no longer show up in the terminal. Starting with Gophish version 0.8.0, you will have the option to configure additional logging directly within Gophish.

In your `config.json` file, modify the `logging` section to include whichever filename you wish to use for logging:

```javascript
"logging": {
	"filename": "gophish.log"
}
```

### Logging to External Sources

By configuring Gophish to send logs to a file, you also create the opportunity to send logs to external sources, such a SIEM. An example would be to use something like [Filebeat](https://www.elastic.co/products/beats/filebeat) to watch the log file and send the entries to an external source of your choosing.

