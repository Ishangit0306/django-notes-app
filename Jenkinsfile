@Library('evon-ci-library') _
evonPipeline(
    application: 'django-notes-app',

    environments: [
        development: [
            branch: 'develop',
            deployPath: '/tmp/django-notes/development'
        ],
        production: [
            branch: 'main',
            deployPath: '/tmp/django-notes/production'
        ]
    ],

    build: [
        type: 'docker',
        composePath: '.'    
    ]
)