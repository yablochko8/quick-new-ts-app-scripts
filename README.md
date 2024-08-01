## How to use this tool

Run the command `npx typespark` in your parent folder for new projects. This script will create the project folder itself.

You will be prompted with the following questions/requests:

1. Give the new app a name:
2. Do you want to use Tailwind for styling? (Y/n)
3. Do you want to add an Express server? (Y/n)
4. [if Yes to Express server] Do you need a PostgreSQL database? (Y/n)

All responses are Yes by default.

## Troubleshooting

If you don't have PM2 installed some conveniences won't work, i.e. the app won't autoload. This will give a minor error message but it's fine.

(PM2 lets you run multiple Node.js applications from a single Terminal window, with a combined view of all their console logs.)

PM2 shows the most recent error logs when you fire it up. This can sometimes be confusing. Use `pm2 flush` to clear out this noise.

## Feature gaps / known issues

### High Priority

1. Fix Tailwind errors in client console:
   0|devclient | warn - No utility classes were detected in your source files. If this is unexpected, double-check the `content` option in your Tailwind CSS configuration.
   0|devclient | warn - https://tailwindcss.com/docs/content-configuration
1. For full-stack projects we need a shared folder at parent level (for types etc) by default
1. Add a better .env default and .env.example
1. Make README.md boilerplate better
1. Make PM2 usage clearer and prompt install, or remove dependency.

### Low Priority

1. Add support for non-Mac (although it may be only the Tailwind sed command that breaks on non-Mac)
1. Fix the test suite part of this script so it works again with the varied folder structure.
