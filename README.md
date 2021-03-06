# Cucumber Coverage

Coverage reporting for cucumber with grunt.

This project is aimed at those using cucumber to execute tests and need to gain coverage information,
while coverage reporters are available for use with tools like selenium and protractor this is aimed at those running tests from the command line.

Configure your tests to execute with cucumber and instrument source code with istanbul to gather coverage information.

This project is aimed to work with both ES5 and ES6 source code projects.

## Getting Started

Get the project as a dependency;

```
npm install --save-dev grunt-cucumber-coverage
```

Add the task to your gruntfile script;

```
grunt.loadNpmTasks('grunt-cucumber-coverage');
```

> Tip: We recommend when using grunt to use the project [load-grunt-tasks](https://www.github.com/sindresorhus/load-grunt-tasks) to simplify your inclusion of grunt task dependencies.

## Usage

*Coming soon*

## Examples

```
cucumber_coverage: {
    example: {
        files: {
            cwd: 'example/features',
            src: '**/*.feature'
        },
        options: {
            coverage: 'example/src'
        }
    }
}
```

## Options

*Coming soon*

## License

Apache 2.0 © [Sysen Limited](http://www.sysen.co.uk)
