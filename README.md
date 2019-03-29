# vuejs-env

When running these commands the results will appear on the startup page.

# File structure
.env                # loaded in all cases
.env.local          # loaded in all cases, ignored by git
.env.[mode]         # only loaded in specified mode
.env.[mode].local   # only loaded in specified mode, ignored by git

### Run the environmental variables for development.
```
npm run serve
```

### Run the environmental variables for development
```
npm run serve -- --mode development
```

### Run the environmental variables for production
```
npm run serve -- --mode production
```
