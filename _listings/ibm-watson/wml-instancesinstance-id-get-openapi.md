---
swagger: "2.0"
x-collection-name: IBM Watson
x-complete: 0
info:
  title: IBM Watson Machine Learning Get Wml Instances Instance
  description: Details about specific service instance
  version: 1.0.0
host: ibm-watson-ml.mybluemix.net
basePath: v3/
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /identity/token:
    get:
      summary: Get Entity Token
      description: Tokens are required for the ML REST API authentication. They are
        generated using ML service credentials
      operationId: generateToken
      x-api-path-slug: identitytoken-get
      responses:
        200:
          description: OK
      tags:
      - Machine Learning
      - Identity
      - Token
    put:
      summary: Put Entity Token
      description: Refreshes token, accepts expired token and generates a new one
        (if the application binding / service key is still valid)
      operationId: refreshes-token-accepts-expired-token-and-generates-a-new-one-if-the-application-binding--service-ke
      x-api-path-slug: identitytoken-put
      parameters:
      - in: body
        name: token
        description: existing token
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Machine Learning
      - Identity
      - Token
  /wml_instances/{instance_id}/published_models:
    get:
      summary: Get Wml Instances Instance Published Models
      description: Get wml instances instance published models.
      operationId: listModelDeployments
      x-api-path-slug: wml-instancesinstance-idpublished-models-get
      parameters:
      - in: query
        name: limit
        description: Maximum number of resources to retrive (defaults to 1000)
      - in: query
        name: start
        description: Token required for token-based pagination
      responses:
        200:
          description: OK
      tags:
      - Machine Learning
      - Wml
      - Instances
      - Instance
      - Id
      - Published
      - Models
  /wml_instances/{instance_id}/published_models/{published_model_id}:
    get:
      summary: Get Wml Instances Instance Published Models Published Model
      description: Get wml instances instance published models published model.
      operationId: details-about-specific-published-model
      x-api-path-slug: wml-instancesinstance-idpublished-modelspublished-model-id-get
      responses:
        200:
          description: OK
      tags:
      - Machine Learning
      - Wml
      - Instances
      - Instance
      - Id
      - Published
      - Models
      - Published
      - Model
      - Id
    delete:
      summary: Delete Wml Instances Instance Published Models Published Model
      description: Delete wml instances instance published models published model.
      operationId: deletes-the-published-model-and-all-its-deployments
      x-api-path-slug: wml-instancesinstance-idpublished-modelspublished-model-id-delete
      parameters:
      - in: query
        name: ignore_spark_errors
        description: If this flag is set to true then deployments of this model will
          be deleted even if spark reports failure in response to kill job request
      responses:
        200:
          description: OK
      tags:
      - Machine Learning
      - Wml
      - Instances
      - Instance
      - Id
      - Published
      - Models
      - Published
      - Model
      - Id
    patch:
      summary: Patch Wml Instances Instance Published Models Published Model
      description: Patch wml instances instance published models published model.
      operationId: updates-the-version-of-deployed-model
      x-api-path-slug: wml-instancesinstance-idpublished-modelspublished-model-id-patch
      parameters:
      - in: body
        name: published_model_patch
        description: Input For Patch
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Machine Learning
      - Wml
      - Instances
      - Instance
      - Id
      - Published
      - Models
      - Published
      - Model
      - Id
  /wml_instances/{instance_id}/published_models/{published_model_id}/evaluation_metrics:
    get:
      summary: Get Wml Instances Instance Published Models Published Model Evaluation
        Metrics
      description: Get wml instances instance published models published model evaluation
        metrics.
      operationId: listModelMetrics
      x-api-path-slug: wml-instancesinstance-idpublished-modelspublished-model-idevaluation-metrics-get
      responses:
        200:
          description: OK
      tags:
      - Machine Learning
      - Wml
      - Instances
      - Instance
      - Id
      - Published
      - Models
      - Published
      - Model
      - Id
      - Evaluation
      - Metrics
  /wml_instances/{instance_id}/published_models/{published_model_id}/learning_configuration:
    put:
      summary: Put Wml Instances Instance Published Models Published Model Learning
        Configuration
      description: Put wml instances instance published models published model learning
        configuration.
      operationId: creates-learning-configuration
      x-api-path-slug: wml-instancesinstance-idpublished-modelspublished-model-idlearning-configuration-put
      parameters:
      - in: body
        name: learning_configuration
        description: The model deployment Id
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Machine Learning
      - Wml
      - Instances
      - Instance
      - Id
      - Published
      - Models
      - Published
      - Model
      - Id
      - Learning
      - Configuration
    patch:
      summary: Patch Wml Instances Instance Published Models Published Model Learning
        Configuration
      description: Patch wml instances instance published models published model learning
        configuration.
      operationId: updates-the-learning-configuration-partially
      x-api-path-slug: wml-instancesinstance-idpublished-modelspublished-model-idlearning-configuration-patch
      parameters:
      - in: body
        name: learning_configuration_patch
        description: Input For Patch
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Machine Learning
      - Wml
      - Instances
      - Instance
      - Id
      - Published
      - Models
      - Published
      - Model
      - Id
      - Learning
      - Configuration
  /wml_instances/{instance_id}/published_models/{published_model_id}/learning_iterations:
    post:
      summary: Post Wml Instances Instance Published Models Published Model Learning
        Iterations
      description: Post wml instances instance published models published model learning
        iterations.
      operationId: evaluateModel
      x-api-path-slug: wml-instancesinstance-idpublished-modelspublished-model-idlearning-iterations-post
      parameters:
      - in: body
        name: learning_iteration_settings
        description: Settings for this particular learning iteration
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Machine Learning
      - Wml
      - Instances
      - Instance
      - Id
      - Published
      - Models
      - Published
      - Model
      - Id
      - Learning
      - Iterations
    get:
      summary: Get Wml Instances Instance Published Models Published Model Learning
        Iterations
      description: Get wml instances instance published models published model learning
        iterations.
      operationId: listModelLearningIterations
      x-api-path-slug: wml-instancesinstance-idpublished-modelspublished-model-idlearning-iterations-get
      parameters:
      - in: query
        name: status
        description: This is the filter parameter which allows to query learning iterations
          with the specific status
      responses:
        200:
          description: OK
      tags:
      - Machine Learning
      - Wml
      - Instances
      - Instance
      - Id
      - Published
      - Models
      - Published
      - Model
      - Id
      - Learning
      - Iterations
  /wml_instances/{instance_id}/published_models/{published_model_id}/learning_iterations/{learning_iteration_id}:
    get:
      summary: Get Wml Instances Instance Published Models Published Model Learning
        Iterations Learning Iteration
      description: Get wml instances instance published models published model learning
        iterations learning iteration.
      operationId: details-about-specific-learning-iteration
      x-api-path-slug: wml-instancesinstance-idpublished-modelspublished-model-idlearning-iterationslearning-iteration-id-get
      responses:
        200:
          description: OK
      tags:
      - Machine Learning
      - Wml
      - Instances
      - Instance
      - Id
      - Published
      - Models
      - Published
      - Model
      - Id
      - Learning
      - Iterations
      - Learning
      - Iteration
      - Id
  /wml_instances/{instance_id}/published_models/{published_model_id}/feedback:
    post:
      summary: Post Wml Instances Instance Published Models Published Model Feedback
      description: |-
        Receives the feedback data and stores it in the feedback store
        defined in learning configuration
      operationId: receives-the-feedback-data-and-stores-it-in-the-feedback-storedefined-in-learning-configuration
      x-api-path-slug: wml-instancesinstance-idpublished-modelspublished-model-idfeedback-post
      parameters:
      - in: body
        name: feedback_data
        description: The feedback data
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Machine Learning
      - Wml
      - Instances
      - Instance
      - Id
      - Published
      - Models
      - Published
      - Model
      - Id
      - Feedback
  /wml_instances/{instance_id}/published_models/{published_model_id}/deployments:
    post:
      summary: Post Wml Instances Instance Published Models Published Model Deployments
      description: Creates the deployment - online, stream, batch (batch deployment
        only supports Cloud Object Storage as input/output for Tensorflow, Keras and
        Caffe models.)
      operationId: creates-the-deployment--online-stream-batch-batch-deployment-only-supports-cloud-object-storage-as-i
      x-api-path-slug: wml-instancesinstance-idpublished-modelspublished-model-iddeployments-post
      parameters:
      - in: body
        name: deployment_input
        description: The input data
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: No Name
      - in: query
        name: sync
        description: This is parameter which determines if the online deployment needs
          to be created in synchronous or asynchronous way
      responses:
        200:
          description: OK
      tags:
      - Machine Learning
      - Wml
      - Instances
      - Instance
      - Id
      - Published
      - Models
      - Published
      - Model
      - Id
      - Deployments
    get:
      summary: Get Wml Instances Instance Published Models Published Model Deployments
      description: Get wml instances instance published models published model deployments.
      operationId: listDeploymentsForModel
      x-api-path-slug: wml-instancesinstance-idpublished-modelspublished-model-iddeployments-get
      parameters:
      - in: query
        name: status
        description: This is the filter parameter which allows to query deployments
          with the specific status
      - in: query
        name: type
        description: This is the filter parameter which allows to query deployments
          with the specific type
      - in: query
        name: _fields
        description: The list of fields which should be included in the response
      responses:
        200:
          description: OK
      tags:
      - Machine Learning
      - Wml
      - Instances
      - Instance
      - Id
      - Published
      - Models
      - Published
      - Model
      - Id
      - Deployments
  /wml_instances/{instance_id}/published_models/{published_model_id}/deployments/{deployment_id}:
    get:
      summary: Get Wml Instances Instance Published Models Published Model Deployments
        Deployment
      description: Get wml instances instance published models published model deployments
        deployment.
      operationId: getDeployment
      x-api-path-slug: wml-instancesinstance-idpublished-modelspublished-model-iddeploymentsdeployment-id-get
      responses:
        200:
          description: OK
      tags:
      - Machine Learning
      - Wml
      - Instances
      - Instance
      - Id
      - Published
      - Models
      - Published
      - Model
      - Id
      - Deployments
      - Deployment
      - Id
    patch:
      summary: Patch Wml Instances Instance Published Models Published Model Deployments
        Deployment
      description: Patch wml instances instance published models published model deployments
        deployment.
      operationId: allows-to-update-the-deployed-stream-status-startstop
      x-api-path-slug: wml-instancesinstance-idpublished-modelspublished-model-iddeploymentsdeployment-id-patch
      parameters:
      - in: body
        name: deployment_patch
        description: Input For Patch
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Machine Learning
      - Wml
      - Instances
      - Instance
      - Id
      - Published
      - Models
      - Published
      - Model
      - Id
      - Deployments
      - Deployment
      - Id
    delete:
      summary: Delete Wml Instances Instance Published Models Published Model Deployments
        Deployment
      description: Delete wml instances instance published models published model
        deployments deployment.
      operationId: ""
      x-api-path-slug: wml-instancesinstance-idpublished-modelspublished-model-iddeploymentsdeployment-id-delete
      parameters:
      - in: query
        name: ignore_spark_errors
        description: If this flag is set to true then the deployment will be deleted
          even if spark reports failure in response to kill job request
      responses:
        200:
          description: OK
      tags:
      - Machine Learning
      - Wml
      - Instances
      - Instance
      - Id
      - Published
      - Models
      - Published
      - Model
      - Id
      - Deployments
      - Deployment
      - Id
  /wml_instances/{instance_id}/published_models/{published_model_id}/deployments/{deployment_id}/online:
    post:
      summary: Post Wml Instances Instance Published Models Published Model Deployments
        Deployment Online
      description: Post wml instances instance published models published model deployments
        deployment online.
      operationId: makes-an-online-prediction-on-a-given-data-values
      x-api-path-slug: wml-instancesinstance-idpublished-modelspublished-model-iddeploymentsdeployment-idonline-post
      parameters:
      - in: body
        name: online_prediction_input
        description: The input data
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Machine Learning
      - Wml
      - Instances
      - Instance
      - Id
      - Published
      - Models
      - Published
      - Model
      - Id
      - Deployments
      - Deployment
      - Id
      - Online
  /wml_instances/{instance_id}/deployments:
    get:
      summary: Get Wml Instances Instance Deployments
      description: Get wml instances instance deployments.
      operationId: listAllDeployments
      x-api-path-slug: wml-instancesinstance-iddeployments-get
      responses:
        200:
          description: OK
      tags:
      - Machine Learning
      - Wml
      - Instances
      - Instance
      - Id
      - Deployments
  /wml_instances/{instance_id}:
    get:
      summary: Get Wml Instances Instance
      description: Details about specific service instance
      operationId: getInstanceDetails
      x-api-path-slug: wml-instancesinstance-id-get
      responses:
        200:
          description: OK
      tags:
      - Machine Learning
      - Wml
      - Instances
      - Instance
      - Id
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---