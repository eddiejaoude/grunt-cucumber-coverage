# Cucumber Coverage

[![Build Status](https://travis-ci.org/sysen-limited/grunt-cucumber-coverage.svg?branch=master)](https://travis-ci.org/sysen-limited/grunt-cucumber-coverage)

Coverage reporting for Node projects using cucumber with grunt.

This project is aimed at those using cucumber to execute tests and need to gain coverage information,
while coverage reporters are available for use with tools like selenium and protractor this is aimed at those running Node tests without a browser.
Both ES5 and ES6 code bases have been tested to ensure current practices are supported.

Runs your tests by executing feature files with [cucumber](https://github.com/cucumber/cucumber-js) and gathers coverage information of source code with [istanbul](https://github.com/gotwarlost/istanbul).

## Getting Started

Get the project as a dependency;

```
npm install --save-dev grunt-cucumber-coverage
```

Add the task to your gruntfile script;

```
grunt.loadNpmTasks('grunt-cucumber-coverage');
```

> Tip:
> We recommend when using grunt to use the project [load-grunt-tasks](https://www.github.com/sindresorhus/load-grunt-tasks) to simplify your inclusion of grunt task dependencies.

## Usage Examples

```
cucumber_coverage: {
    example: {
        src: 'example/features',
        options: {
            coverage: 'example/src',
            check: {
                lines: 100,
                statements: 100,
                functions: 100,
                branches: 100
            },
            steps: 'example/features/step_definitions',
            tags: '~@Ignore'
        }
    }
}

grunt.registerTask('test', ['cucumber_coverage']);
```

> Note:
> The **src** value should be set to the location of your cucumber / feature files.

## Options

### options.coverage
This is the source code folder for which coverage reporting will be made.

Type: `String`
Default: `null`

### options.check
This enables coverage checking of thresholds, if set to true then default values are used.

Type: `Object` or `Boolean`
Default: `false`

| key | default |
| :--- | :--- |
| lines | 80 |
| statements | 80 |
| functions | 80 |
| branches | 80 |

> Hint:
> You can also change just individual keys if required and defaults will be used for others.

> Note:
> The default **false** value will mean that coverage levels are not checked and low coverage will not result in a grunt error.

### options.steps
Specify where step definitions are located from project root directory

Type: `String`
Default: `src` + `/` + `step_definitions`

### options.tags
Run just a specific tag or tags for a feature file set

Type: `String` or `Array`
Default: `null`

> Hint:
> Run just one tag `@tag`
> Run several tags `@tag,@special`
> Exclude a tag `~@ignore`
> Run a mix `['@tag,@special', '~@ignore']`

## License

Apache 2.0 © [Sysen Limited](http://www.sysen.co.uk)
