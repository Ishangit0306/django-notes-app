@Library('evon-jenkins-shared-library@main') _

evonPipeline(
    application: 'django-notes-app',

    environments: [
        staging: [
            branch: 'develop',
            deployPath: '/tmp/django-notes/staging'
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