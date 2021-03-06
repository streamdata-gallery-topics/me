---
swagger: "2.0"
x-collection-name: AWS Inspector
x-complete: 0
info:
  title: AWS Inspector API List Assessment Run Agents
  version: 1.0.0
  description: |-
    Lists the agents of the assessment runs that are specified by the ARNs of the
             assessment runs.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=CreateAssessmentTarget:
    get:
      summary: Create Assessment Target
      description: |-
        Creates a new assessment target using the ARN of the resource group that is generated
                 by.
      operationId: createAssessmentTarget
      x-api-path-slug: actioncreateassessmenttarget-get
      parameters:
      - in: query
        name: assessmentTargetName
        description: The user-defined name that identifies the assessment target that
          you want to create
        type: string
      - in: query
        name: resourceGroupArn
        description: The ARN that specifies the resource group that is used to create
          the assessment         target
        type: string
      responses:
        200:
          description: OK
      tags:
      - Assessment Targets
  /?Action=CreateAssessmentTemplate:
    get:
      summary: Create Assessment Template
      description: |-
        Creates an assessment template for the assessment target that is specified by the ARN
                 of the assessment target.
      operationId: createAssessmentTemplate
      x-api-path-slug: actioncreateassessmenttemplate-get
      parameters:
      - in: query
        name: assessmentTargetArn
        description: The ARN that specifies the assessment target for which you want
          to create the         assessment template
        type: string
      - in: query
        name: assessmentTemplateName
        description: The user-defined name that identifies the assessment template
          that you want to         create
        type: string
      - in: query
        name: durationInSeconds
        description: The duration of the assessment run in seconds
        type: string
      - in: query
        name: rulesPackageArns
        description: The ARNs that specify the rules packages that you want to attach
          to the assessment         template
        type: string
      - in: query
        name: userAttributesForFindings
        description: The user-defined attributes that are assigned to every finding
          that is generated by         the assessment run that uses this assessment
          template
        type: string
      responses:
        200:
          description: OK
      tags:
      - Assessment Templates
  /?Action=DeleteAssessmentRun:
    get:
      summary: Delete Assessment Run
      description: |-
        Deletes the assessment run that is specified by the ARN of the assessment
                 run.
      operationId: deleteAssessmentRun
      x-api-path-slug: actiondeleteassessmentrun-get
      parameters:
      - in: query
        name: assessmentRunArn
        description: The ARN that specifies the assessment run that you want to delete
        type: string
      responses:
        200:
          description: OK
      tags:
      - Assessment Runs
  /?Action=DeleteAssessmentTarget:
    get:
      summary: Delete Assessment Target
      description: |-
        Deletes the assessment target that is specified by the ARN of the assessment
                 target.
      operationId: deleteAssessmentTarget
      x-api-path-slug: actiondeleteassessmenttarget-get
      parameters:
      - in: query
        name: assessmentTargetArn
        description: The ARN that specifies the assessment target that you want to
          delete
        type: string
      responses:
        200:
          description: OK
      tags:
      - Assessment Targets
  /?Action=DeleteAssessmentTemplate:
    get:
      summary: Delete Assessment Template
      description: |-
        Deletes the assessment template that is specified by the ARN of the assessment
                 template.
      operationId: deleteAssessmentTemplate
      x-api-path-slug: actiondeleteassessmenttemplate-get
      parameters:
      - in: query
        name: assessmentTemplateArn
        description: The ARN that specifies the assessment template that you want
          to delete
        type: string
      responses:
        200:
          description: OK
      tags:
      - Assessment Templates
  /?Action=DescribeAssessmentRuns:
    get:
      summary: Describe Assessment Runs
      description: |-
        Describes the assessment runs that are specified by the ARNs of the assessment
                 runs.
      operationId: describeAssessmentRuns
      x-api-path-slug: actiondescribeassessmentruns-get
      parameters:
      - in: query
        name: assessmentRunArns
        description: The ARN that specifies the assessment run that you want to describe
        type: string
      responses:
        200:
          description: OK
      tags:
      - Assessment Runs
  /?Action=DescribeAssessmentTargets:
    get:
      summary: Describe Assessment Targets
      description: |-
        Describes the assessment targets that are specified by the ARNs of the assessment
                 targets.
      operationId: describeAssessmentTargets
      x-api-path-slug: actiondescribeassessmenttargets-get
      parameters:
      - in: query
        name: assessmentTargetArns
        description: The ARNs that specifies the assessment targets that you want
          to describe
        type: string
      responses:
        200:
          description: OK
      tags:
      - Assessment Targets
  /?Action=DescribeAssessmentTemplates:
    get:
      summary: Describe Assessment Templates
      description: |-
        Describes the assessment templates that are specified by the ARNs of the assessment
                 templates.
      operationId: describeAssessmentTemplates
      x-api-path-slug: actiondescribeassessmenttemplates-get
      parameters:
      - in: query
        name: assessmentTemplateArns
        description: 'Type: array of Strings'
        type: string
      responses:
        200:
          description: OK
      tags:
      - Assessment Templates
  /?Action=GetTelemetryMetadata:
    get:
      summary: Get Telemetry Metadata
      description: |-
        Information about the data that is collected for the specified assessment
                 run.
      operationId: getTelemetryMetadata
      x-api-path-slug: actiongettelemetrymetadata-get
      parameters:
      - in: query
        name: assessmentRunArn
        description: The ARN that specifies the assessment run that has the telemetry
          data that you want         to obtain
        type: string
      responses:
        200:
          description: OK
      tags:
      - Telemetry Metadata
  /?Action=ListAssessmentRunAgents:
    get:
      summary: List Assessment Run Agents
      description: |-
        Lists the agents of the assessment runs that are specified by the ARNs of the
                 assessment runs.
      operationId: listAssessmentRunAgents
      x-api-path-slug: actionlistassessmentrunagents-get
      parameters:
      - in: query
        name: assessmentRunArn
        description: The ARN that specifies the assessment run whose agents you want
          to list
        type: string
      - in: query
        name: filter
        description: You can use this parameter to specify a subset of data to be
          included in the actions         response
        type: string
      - in: query
        name: maxResults
        description: You can use this parameter to indicate the maximum number of
          items that you want in         the response
        type: string
      - in: query
        name: nextToken
        description: You can use this parameter when paginating results
        type: string
      responses:
        200:
          description: OK
      tags:
      - Assessment Run Agents
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