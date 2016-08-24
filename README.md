# datapact-resource

Lightweight data processing executed by Concourse using a git repository to store state and S3 to store results.

Say you have a project which will regularly be bulk processing data.

# File Format

    {
        "branch": "{{ string }}",
        "run": {
            "started": "{{ iso8601 }}",
            "finished": "{{ iso8601 }}",
            "duration": {{ number }},
            "metadata": {{ object }}
        },
        "input": [
            {
                "name": "{{ string }}",
                "branch": "{{ string }}",
                "run": "{{ string }}"
            },
            ...
        ],
        "output": [
            {
                "path": "{{ string }}",
                "size": {{ number }},
                "sha256": "{{ string }}",
                "filters": [
                    "{{ string }}",
                    ...
                ]
            },
            ...
        ]
    }
