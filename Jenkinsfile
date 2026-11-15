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
        composePath: '.',

        images: [
            [
                name: 'django-notes-app',
                environmentVariable: 'APP_IMAGE'
            ],
            [
                name: 'django-notes-nginx',
                environmentVariable: 'NGINX_IMAGE'
            ]
        ]
    ],

    registry: [
        type: 'dockerhub',
        credentialsId: 'dockerhub-credentials',
        namespace: 'ishan0305'
    ]
)