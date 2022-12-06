# Change Log
All notable changes to this project will be documented in this file, which follows the guidelines
on [Keep a CHANGELOG](http://keepachangelog.com/). This project adheres to
[Semantic Versioning](http://semver.org/).

## [11.0.0-M29] - 2022-11-30
### Changed
- Close the client in DefaultRestClientProcessor

## [11.0.0-M28] - 2022-11-23
### Changed
- Removed log4j-over-slf4j as it is now replaced by slf4j-reload4j

## [11.0.0-M27] - 2022-11-22
### Security
- Update common bom to 11.0.0-M20 in order to:
    - Update hibernate version to 5.4.24.Final
    - Update jackson.databind version to 2.12.7.1

## [11.0.0-M26] - 2022-11-18
### Changed
- Update common bom to 11.0.0-M19 in order to:
    - Update jackson libraries to 2.12.7

## [11.0.0-M24] - 2022-11-16
### Changed
- Update common bom to 11.0.0-M18 in order to:
    - Update jboss-logging version to 3.5.0.Final

## [11.0.0-M23] - 2022-11-10
### Added
- Add messaging-jms dependency to framework-bom

## [11.0.0-M22] - 2022-11-03
### Security
- Updates to various libraries to address security alerts:
    - wildfly to version 26.1.2.Final
    - artemis to version 2.20.0
    - resteasy-client to version 4.7.7.Final

## [11.0.0-M21] - 2022-10-18
### Changed
- Updated slf4j/log4j bridge jar from slf4j-log4j12 to slf4j-reload4j

## [11.0.0-M20] - 2022-09-05
### Changed
- MessageProducerClient is now idempotent when calling `startProducer(...)`

## [11.0.0-M19] - 2022-08-31
### Added
- Added MessageProducerClientBuilder for creating configurable message producer clients
### Changed
- Update framework-libraries to 11.0.0-M20 for:
    - A default name of `jms.queue.DLQ` rather than the original name of `DLQ`
    - A new constructor to pass the name in if you don't want the default name
    - New builder `MessageConsumerClientBuilder` that allows ActiveMQ connection parameters to be specified

## [11.0.0-M18] - 2022-08-12
### Changed
- Update common bom to 11.0.0-M15 in order to:
    - Update artemis-jms-client to 2.10.1

## [11.0.0-M17] - 2022-06-16
### Added
- Added a utility in healthchecks for checking the names of tables in a postgres database

## [11.0.0-M16] - 2022-06-08
### Changed
- Update framework-libraries to version 11.0.0-M18

## [11.0.0-M15] - 2022-05-30
### Changed
- Removed strict checking of liquibase.properties files

## [11.0.0-M14] - 2022-05-23
### Changed
- Update maven-framework-parent-pom to 11.0.0-M6

## [11.0.0-M13] - 2022-05-20
### Changed
- Update liquibase to 4.10.0

## [11.0.0-M11] - 2022-03-25
### Fixed
- Healthchecks how return json with correct UTF-8 charset

## [11.0.0-M10] - 2022-03-23
### Changed
- Update framework-libraries to version 11.0.0-M13

### Changed
## [11.0.0-M9] - 2022-03-22
- Added mechanism for running better healthchecks

## [11.0.0-M8] - 2022-03-16
- Fix Jmx Command Client to run with Wildfly 20.0.1
- Update to log4j 2

## [11.0.0-M7] - 2022-02-25
### Changed
- Update framework-libraries to allow
    - Update log4j2 to 2.17.1 to fix critical security violation

## [11.0.0-M6] - 2021-06-15
### Changed
- Update framework-libraries to 11.0.0-M7

## [11.0.0-M5] - 2021-05-28
### Changed
- Update framework-libraries to 11.0.0-M6

## [11.0.0-M4] - 2021-05-18
### Changed
- Update framework-libraries to 11.0.0-M5

## [11.0.0-M3] - 2021-05-07
### Changed
- Update framework-libraries to 11.0.0-M4
- Update maven-framework-parent-pom to 11.0.0-M3
- Fixed all tests affected by the update to OpenEjb 8.0.6

## [11.0.0-M2] - 2021-02-04
### Changed
- Update to JEE 8
- Update framework-libraries to 11.0.0-M2

## [11.0.0-M1] - 2021-01-26
### Changed
- Update framework-parent-pom to 11.0.0-M1
- Update framework-libraries to 11.0.0-M1

## [8.0.0-M3] - 2021-01-06
### Changed
- Update framework-libraries to 8.0.0-M3

## [8.0.0-M2] - 2021-01-06
### Changed
- Update framework-libraries to 8.0.0-M2

## [8.0.0-M1] - 2021-01-04
### Changed
- Update to OpenJDK 11
- Update framework-libraries to 8.0.0-M1
- Update framework-parent-pom to 8.0.0-M2

## [7.2.23] - 2021-03-29
### Changed
- RestClientProcessor now handles bad request (400) responses by throwing a BadRequestException

## [7.2.2] - 2020-11-18
### Added
- New JNDI variable `feature-control.enabled` for enabling/disabling of remote fetching of Features
- Moved in EmptyFeatureFetcher from framework-api

## [7.2.1] - 2020-11-18
### Added
- New JNDI variable `feature-control-cache.enabled` to control whether the results
  of the fetch of Features are cached
### Changed
- The caching of features is now disabled by default
- Updated framework-libraries to version 7.2.1

## [7.2.0] - 2020-11-13
### Added
- Support for FeatureControl toggling by annotating service component
  handler methods with @FeatureControl
- New timer bean for fetching and storing of feature control Features
- New SystemCommand `REFRESH_FEATURE_CACHE` to force a refresh of the Feature Control cache
### Changed
- Updated framework-libraries to version 7.2.0

## [7.1.4] - 2020-10-16
### Changed
- Updated framework-libraries to version 7.1.5
    - Builders of generated pojos now have a `withValuesFrom(...)` method
      to allow the builder to be initialised with the values of another pojo instance

## [7.1.3] - 2020-10-14
### Changed
- Security updates to apache.tika, commons.beanutils, commons.guava and junit in common-bom
- Updated common-bom to 7.1.1

## [Unreleased]
## [7.1.2] - 2020-10-09
### Changed
- Raml-lint-checker will now allow handler methods whose names are not specified in the
  raml file if the handler name starts with 'administration'
- Updated framework-libraries to version 7.1.2

## [7.1.1] - 2020-09-25
### Changed
- Updated framework-libraries to version 7.1.1

## [7.1.0] - 2020-09-23
### Changed
- Updated parent maven-framework-parent-pom to version 2.0.0
- Updated framework-libraries to version 7.1.0
- Moved to new Cloudsmith.io repository for hosting maven artifacts
- Updated encrypted properties in travis.yaml to point to cloudsmith

## [7.0.11] - 2020-09-10
### Changed
- Update to framework-libraries 7.0.11

## [7.0.10] - 2020-08-14
### Changed
- Fix of hanging deployment in wildfly caused by using @Singleton annotation
  on a class that is called by wildfly Observer/Observable event architecture

## [7.0.9] - 2020-08-13
### Added
- Added a separate Jms sender for Audit
- The Audit JMS Connection Factory will now only be used
  if the Correct JNDI property `jms.connection.audit.message.broker.enabled'
  is set to true


## [7.0.8] - 2020-07-24
### Added
- New JNDI property `rest.dispatcher.response.json.validation.enabled` to
  enable/disable rest json response validation in the query pillar. Disabled
  by default

## [7.0.7] - 2020-07-07
### Changed
- Update to framework-libraries 7.0.9

## [7.0.6] - 2020-06-03
### Changed
- Update to framework-libraries 7.0.8

## [7.0.5] - 2020-05-29
### Changed
- Update to framework-libraries 7.0.7

## [7.0.4] - 2020-05-27
### Changed
- Updated to framework-libraries 7.0.5
### Added
- Added metrics dependencies to the bom

## [7.0.3] - 2020-05-21
### Changed
- Change dependencies to only depend on framework-libraries 7.0.4

## [7.0.1] - 2020-05-18

### Changed
- Update maven common bom version to 2.5.0
- Update framework-api version to 7.0.0
- Update framework-utilities version to 7.0.1
- Update framework-libraries version to 7.0.1
- Combined the following repos into microservice-framework
  microservice_framework_version_6
  framework-generators
  framework-jmx-command-client
  mertrics

### Added
- microservice_framework_version_6 6.4.2: now set to version 7.0.0
- framework-generators 2.4.4: now set to version 7.0.0
- framework-jmx-command-client 2.4.2: now set to version 7.0.0
- metrics 3.3.2: now set to version 7.0.0

## [6.4.2] - 2020-04-23
### Changed
- Update framework-api to 4.3.0

## [6.4.1] - 2020-04-09
### Added
- Added get file-service datasource to TestJdbcDataSourceProvider

## [6.4.0] - 2019-11-12
### Changed
- SHUTTER command renamed to SUSPEND
- UNSHUTTER command renamed to UNSUSPEND

## [6.3.0] - 2019-11-07
### Changed
- JMX client is now called using the command name as a String rather than the SystemCommand itself.
- SystemCommands moved out to the projects that contain their CommandHandlers rather than centralised in
  framework.

## [6.2.5] - 2019-11-04
### Changed
- Update json-schema-catalog to 1.7.6

## [6.2.4] - 2019-11-04
### Added
- New command ValidatePublishedEventsCommand that is for checking that all events fulfil their schemas

## [6.2.3] - 2019-10-31
### Changed
- Commands now fail with an UnrunnableSystemCommandException if the command is already in progress

## [6.2.2] - 2019-10-23
### Added
- New SystemCommands EnablePublishingCommand and DisablePublishingCommand for enabling/disabling the publishing beans
### Changed
- Updated utilities.version to 1.20.3
- Updated json schema catalog to 1.7.5

## [6.2.1] - 2019-10-17
### Changed
- Renamed SystemCommandFailedException to SystemCommandInvocationFailedException
  for better exception handling in the JMX client

## [6.2.0] - 2019-10-15

### Added
- JMX bean can now be pinged to get command status:
    - COMMAND_RECEIVED
    - COMMAND_IN_PROGRESS
    - COMMAND_COMPLETE
    - COMMAND_FAILED
- Added commandId to all SystemEvents
- All Shuttering Executors now implement the ShutteringExecutor interface
- New table in the system database 'system_command_status'

### Changed
- All commands now have state that can be queried by the JMX client
- MDC service component logging interceptor
- EventCatchupCommand and IndexerCatchupCommand now both have a common interface: CatchupCommand
- ShutterCommand and UnshutterCommand now both have a common interface: ApplicationShutteringCommand

## [6.1.2] - 2019-10-04
### Changed
- Storing of Commands whilst shuttered is now idempotent
- Do not shutter the JmsEnvelopeSender when called from the Command-Controller component

## [6.1.1] - 2019-10-01
### Added
- Injectable debug logger that logs only if debug logging is set.

## [6.1.0] - 2019-09-28
### Changed
- All SystemCommandHandler methods now also take a mandatory commandId as a parameter
- SystemCommander JMX bean now returns a unique command id for each command that it runs

## [6.0.16] - 2019-09-23
### Changed
- Renamed ValidateCatchupCommand to VerifyCatchupCommand
- Added MBeanClientConnectionException to the JMX client classes to show that a connection error occurred

## [6.0.15] - 2019-09-19
### Added
- New SystemCommands: AddTriggerCommand, RemoveTriggerCommand and ValidateCatchupCommand
### Changed
- Updated framework-api to 4.1.0

## [6.0.14] - 2019-09-11
### Changed
- System commands now run using a ManagedExecutor rather than an asynchronous EJB

## [6.0.13] - 2019-09-10
### Changed
- SystemCommandStore moved to an interface implemented by DefaultSystemCommandStore. This is to allow stubbing in integration tests

## [6.0.12] - 2019-09-08
### Changed
- All JMX SystemCommands are now run asynchronously. i.e the call to the JMX bean will return immediately
- The JMX SystemCommandBean now only throws 2 Exceptions
    1. UnsupportedSystemCommandException. If the command is unrecognised by the context.
    2. SystemCommandFailedException. On any other failure. NB. this Exception also contains the stacktrace of the server side exception

## [6.0.11] - 2019-08-30
### Added
- ordering to subscriptions descriptor yamls

### Fixed
- JdbcDataSourceProvider can now handle multiple DataSources

## [6.0.10] - 2019-08-28
### Added
- JMX SystemCommands can now be disabled for a context

## [6.0.9] - 2019-08-21
### Fixed
- JsonSchemaValidationMatcher now supports yaml/json/schema location

## [6.0.8] - 2019-08-21
### Fixed
- Better error message if the name of the JMX bean is incorrect when called by the client

## [6.0.7] - 2019-08-20
### Added
- New Utility test class for calling SystemCommands
### Changed
- Name SystemCommand classes have consistent name. i.e. from ShutterSystemCommand to ShutterCommand
- The the context name in JmxParameters is now parsed so that everything after the first dash is excluded
  i.e. a war with name 'customer-service' would now become just 'customer'
### Fixed
- All server side Exceptions thrown by the JMX bean are now included in the api classes to fix
  ClassNotFoundExceptions in the JMX client

## [6.0.6] - 2019-08-19
### Removed
- ApplicationShutteredStateObserver so that state is not changed by observed events

## [6.0.5] - 2019-08-19
### Changed
- Shuttering state is now set directly rather than relying on Events as they may arrive out of order

## [6.0.4] - 2019-08-16
### Added
- New call to get application state from JMX bean

## [6.0.3] - 2019-08-16
### Added
- subscriptions_descriptor.yaml location pattern for jms_uri and rest_uri
### Fixed
- Fixed PING system command
- ShutteringRegistry is now correctly a singleton
### Added
- New jmx test-utils modulue with factory for running the jmx client classes in tests

## [6.0.2] - 2019-08-15
### Changed
- Update json-schema-catalog to 1.7.4

## [6.0.1] - 2019-08-15
### Changed
- Update utilities to 1.20.2

## [6.0.0] - 2019-08-15
### Changed
- Catchup and Rebuild fully implemented using JMX
- SystemCommand mechanism to allow us to call management commands on the framework via JMX
- New System Command to Shutter application
- New System Command to run Catchup
- New System Command to run Rebuild
- New System Command to run Indexes Catchup
- New System database
- New method to list all SystemCommands added to SystemCommander JmxBean
- Brought in jmx command client code from cake-shop
- JMX bean command handlers for system commands
- Observers for the shutter then catchup process
- JmsQueueBrowser service to return the size of a queue
- New jmx test-utils modulue with factory for running the jmx client classes in tests
- All commands received whilst the application is shuttered are stored in a new table 'shuttered_command_store' in the viewstore
- Stored commands are send to JMS once the application is un-shuttered
- Rename ComponentNameUtil to ComponentNameExtractor and moved to common
- Renamed JdbcRepositoryHelper to JdbcResultSetStreamer
- Extracted preparedStatementWrapperOf() in JdbcRepositoryHelper to a new class 'PreparedStatementWrapperFactory'
- Remove validation info logging
- Merged in Subscription domain, yaml parsing classes and builders from event-store
- JmsEnvelopeSenderProducer provides shuttering JmsEnvelopeSender by default to components, non component injection point will be provided with a non shuttering JmsEnvelopeSender
- Jmx client classes now use proper dependency injection
- The context name is now used in the registration name of the SystemCommander MBeans
- Moved InvalidHandlerMethodException to jmx-api to allow it to be caught
  in the command line jmx client
- Shuttering of a context is idempotent
- Extracted SystemCommands into their own module jmx-api
- rest_uri in event-sources.yaml is now optional to support JMS only sources
- If authentication fails when connecting to JMX then a specific exception 'JmxAuthenticationException' is thrown
- Update common-bom to 2.4.0
- Update framework-api 4.0.0
- Update utilities to 1.20.1
- Update json-schema-catalog to 1.7.4
- Update json-pojo-generator to 1.7.2
- Update file-service to 1.17.11
- Update test-utils to 1.24.2
- Update json-transformer to 1.0.7

### Removed
- Removed all deprecated classes and methods
- Remove test-utils-wildfly module
- Event subscription now depends on utilities for YAML parser

## [5.2.0] - 2019-02-13
### Added
- Add pojo implementation for Sender, Requester to DispatcherDelegate class
### Changed
- Updated HandlerMethodMatcher class to support pojo envelope

## [5.1.1] - 2019-02-04
### Changed
- Updated to common-bom to 1.29.0
- Updated to test-utils to 1.22.0
- Updated to utilities to 1.16.4
- Updated to json-schema-catalog to 1.4.5
- Updated to framework-api 3.2.0

### Removed
- wildfly-vfs module - VfsResolverStrategy class
- FileSystemUrlResolverStrategy interface

## [5.1.0] - 2019-01-08
### Changed
- Updated to test-utils to 1.19.1
- Updated to utilities to 1.16.2
- Updated to framework-api 3.1.0
### Added
- Implementation of Metadata interface adding eventNumber and previousEventNumber
- JsonValueEnvelopeMatcher for matching Envelope<JsonValue> types
### Removed
- Removed ReflectionUtils: use ReflectionUtil in test-utils instead

## [5.0.4] - 2018-11-15
### Added
- setInt method to PreparedStatementWrapper

### Changed
- Update framework-api to 3.0.1
- Set high priority to the EnveloperTestProvider

## [5.0.3] - 2018-11-09
### Changed
- Update test-utils to 1.18.1
- Update utilities to 1.16.1
- Update json-schema-catalog to 1.4.2
- Update framework-api to 3.0.0

## [5.0.2] - 2018-11-07

### Changed
- Fix base pom dependencies

## [5.0.1] - 2018-11-07
### Changed
- Update framework-api to version 3.0.0

## [5.0.0] - 2018-11-07
### Removed
- Aggregate to its own repository: https://github.com/CJSCommonPlatform/framework-domain
- Event Store to its own repository: https://github.com/CJSCommonPlatform/event-store
- Generators to their own repository: https://github.com/CJSCommonPlatform/framework-generators
- Cake Shop example app to its own repository: https://github.com/CJSCommonPlatform/cake-shop
- AbstractJdbcRepositoryIT from test utils, deprecated in previous version
- Moved CDI producers to [Utilities](https://github.com/CJSCommonPlatform/utilities)

### Changed
- Message adapter generator to use SubscriptionManager instead of the interceptor chain
- Travis setup now creates a postgres database as part of the build
- Moved EventBuffer into DefaultSubscriptionManager
- Moved persistence-test-utils to event-store
- Updated to use latest raml generator plugin
- Updated utilities version to 1.15.1
- Updated test-utils version to 1.17.2
- Updated file.service version to 1.16.4
- Updated json-schema-catalog version to 1.4.1
- Updated common-bom version to 1.26.0 for Jackson version 2.8.11
- Updated maven framework parent pom version to 1.12.2
- Updated raml maven plugin version to 1.6.2
- Updated generator maven plugin version to 2.5.0
- Reduce the logging level for not using schema catalog
- Moved Integration tests in Event Buffer to use the new postgress database rather then H2 in memory database
- Integration Tests now use a running local instance of Postgres, rather than using an in memory database
- Updated common-bom version to 1.27.0 to fix apache tika security issues
- Update JdbcEventRepository to return all active stream ids

### Added
- Schema catalog generation plugin to example service
- SchemaCatalogResolver to JsonSchemaLoader for resolving file base schemas with the schema catalog
- test-utils-enveloper-provider module
- EnveloperTestProvider that is used for testing usage of the Enveloper
- Flag to disable running of Integration Tests as part of the build
- Ability to return an Accepted code and payload from a post to a Command API component

## [4.3.2] - 2018-07-11
### Changed
- Upgraded generator maven plugin to version 2.6.0
- Upgraded json schema catalog to version 1.3.2

## [4.3.1] - 2018-07-11
### Added
- Ability to return an Accepted code and payload from an post to a Command API component

### Changed
- Remove logging to keep within Travis 4MB log limit

## [4.2.2] - 2018-07-05
### Changed
- Add SchemaCatalogResolver to JsonSchemaLoader for resolving file base schemas with the schema catalog

## [4.2.1] - 2018-06-21
### Changed
- Updated framework-api version to 2.1.2 to fix apache tika security issues

## [4.2.0] - 2018-06-21
### Added
- Added a page size when reading stream of events
### Changed
- Updated framework-api to 2.1.1
- Updated common-bom version to 1.27.0 to fix apache tika security issues

## [4.1.2] - 2018-06-11
### Fixed
- Fix incorrect insertion of stream status table containing one record for unknown and correct source

## [4.1.1] - 2018-06-05
### Fixed
- Update of stream status table now handles a source column of 'unknown'

## [4.1.0] - 2018-05-24
### Added
- Update JdbcEventRepository to return all active stream ids

## [4.0.7] - 2018-05-22
### Fixed
- Event Buffer stream status version update issue

## [4.0.6] - 2018-05-21
### Fixed
- Schema Validation Exception not caught error

## [4.0.5] - 2018-05-18
### Fixed
- Upgrade parent pom to fix upgrade of Jackson 2.8.11

### Changed
- Reduce the logging level for not using schema catalog

## [4.0.4] - 2018-05-17
### Changed
- Upgrade Jackson to 2.8.11 to fix Jackson security issues

## [4.0.3] - 2018-05-10
### Changed
- Makes TestDataSourceFactory lock rows in the same way as postgresql
- Makes TestDataSourceFactory more extensible through overloaded createDataSource methods
### Fixed
- Tests for test-utils-pseristence were not in correct maven file structure so unused
- Minor fixes to test-utils-pseristence tests where components have changed

## [4.0.2] - 2018-05-02
### Changed
- Caches mapping between media types and action names for the schema catalog are now lazy loaded

## [4.0.1] - 2018-04-20
### Added
- StreamId now persisted by enveloper for metadata

## [4.0.0] - 2018-03-09

### Added
- Schema catalog generation plugin to example service

### Changed
- Randomise JMS and HTTP ports for integration tests
- Move LoggerUtils to utilities as part of rest-adapter dependency update
- Remove dependencies on core in messaging-adapter-core and partly in rest-adapter-core
- Move DefaultJsonValidationLoggerHelper to core
- Use JsonSchemaValidatonException instead of org.everit.json.schema.ValidationException
- SPI for InterceptorContext.interceptorContextWithInput()

## [3.1.0] - 2018-01-23

### Fixed
- Reinstate TestEventRepository test utility.

## [3.0.0] - 2018-01-18

### Added
- JsonEnvelope and Metadata builder service provider
- Introduced event_stream table to the event-store, with accompanying repository and services
- Event-Store Restful API, including paginated feeds
- POJO support to HandlerMethods
- Event-Store operations for cloning, clearing and marking streams as inactive
- Add schema catalog generation and validation

### Changed
- Switched to use Apache commons-lang3 library instead of commons-lang
- Update dependencies for OWASP fixes
- Upgraded example application to deploy as a Single war
- Updated example application schemas to avoid conflicts when deployed as a single war
- Convenience methods to JsonEnvelope for providing JsonEnvelopes and JsonObjectMetadataBuilders
- MetadataBuilderFactory in test-utils-core which contains convenience methods for creating
  JsonObjectMetadataBuilders in tests
- InterceptorChainEntryProvider to be used instead of InterceptorChainProvider

### Removed
- Moved framework-api into a new [repository](https://github.com/CJSCommonPlatform/framework-api)
- Moved metrics into a new [repository](https://github.com/CJSCommonPlatform/metrics)
- Component modules and Interceptor chain providers
- Unused dependencies, such as hamcrest-date

## [2.5.3] - 2018-01-11
### Fixed
- Backwards compatible issue with JsonSchemaValidator

## [2.5.2] - 2018-01-08
### Changed
- Now using maven-framework-parent-pom 1.10.1

## [2.5.1] - 2018-01-03
### Added
- Now generating mapping file for action name to media type, used when validating requests


## [2.5.0] - 2017-12-15
### Added
- Catalog generation for all json schema files. Add an id into a json schema to use.

## [2.4.3] - 2017-12-11
### Changed
- Upgrade File Service to 1.14.0
- Upgrade Utilities to 1.11.0
- Upgrade Test Utils to 1.15.0

## [2.4.2] - 2017-12-08

### Fixed
- The issue, where there are no schema validations of command handler due to single war class loading EventFilter of Event Listener for handlers which then skips validation due to no match on the names with events.

## [2.4.1] - 2017-11-06

### Changed
- Removed duplicated test utilities from test-utils module
- Use test-utils project version of test utilities
- Use latest release versions of dependencies to fix OWASP vulnerabilities

## [2.3.2] - 2017-10-17

##Changed
Replaced the JsonObjectObfuscator with the version from utilities that is based on javax.json

## [2.3.1] - 2017-10-12

### Changed
- Deprecate DefaultJsonEnvelope, JsonObjectBuilderWrapper and JsonObjectMetadata
- Deprecate JavaCompilerUtil
- Utilities library upgraded to 1.8.1 and file service to 1.11.1 to pick up JSON logging fix
- Deprecate InterceptorChainProvider

### Removed
- org.apache.commons commons-lang3 dependency from core

## [2.2.1] - 2017-09-01

### Changed
- Converted to release to bintray
- Converted example context to run as a single war by default

### Fixed
- Class conflicts between generated clients in a single war

## [2.2.0] - 2017-08-02

### Changed
- Use maven-framework-parent-pom 1.6.1, which simply changes the wildfly-maven-plugin to 1.2.0.Alpha6 and stops adding it to every build
- example-it: move the wildfly operations to the pre/post-integration-test phases (where they belong)
- Switch to bintray for release processes
- Cleaned up some unnecessary version overrides

## [2.1.0] - 2017-07-17

### Added
- New test matcher for checking schema properties

### Fixed
- Aggregate snapshot repository did not use aggregate class when retrieving snapshots, so services that use multiple aggregate classes
  on the same stream could get class cast exceptions

## [2.0.0] - 2017-06-23

### Changed
- Refactor all framework components that are not internal so that they are provided as interfaces
  via new Framework API modules
- Rework interceptor chain so that it is specific to a service component, by allowing each component
  to provide an interceptor chain definition rather than using annotation scanning
- Upgrade to use framework parent POM [1.5.0](https://github.com/CJSCommonPlatform/maven-framework-parent-pom/releases/tag/release-1.5.0)
- Upgrade to use common BOM [1.16.0](https://github.com/CJSCommonPlatform/maven-common-bom/releases/tag/release-1.16.0)
- Interceptor chain now adds the component name to the context so it can be used by the access control interceptor or anything else that needs it
- Logging dependencies tidied up - all logging implementations excluded from dependencies and tests use new test utils modules for logging
- Generated class names made more unique, including adding the base URI in class name for generated JMS listeners. **Any project that overrides the generated
  class will need to change the class name of their override to match**
- Improved logging for annotation scanning
- Add component to audit interceptor so that audit messages can distinguish between components even
  when they are deployed in a single WAR.

### Removed
- Support for default sender destinations removed; senders now always require messaging clients to
  be provided, typically by generating one from the destination RAML.
- Access control Provider annotation and annotation scanning; this functionality has moved to the access control library
- Precondition class marked as deprecated - will be removed in 3.0.0 unless a different use case is found for it

### Fixed
- Test cases for random ZonedDateTime generators and added logging to show more info when they fail
- Javadoc errors
- Aggregate snapshot service was pulling in Liquibase due to an incorrect dependency scope
- Remove audit from event listener and event processor

### Added
- Script for building dependencies locally
- Support for generating and discovering direct adapters, if a message destination exists locally
  a service component in the same application

## [2.0.0-rc8] - 2017-06-23

### Fixed
- Remove audit from event listener and event processor

## [2.0.0-rc7] - 2017-06-23
### Changed
- Message client generated class name no longer enforces base URI pattern

## [2.0.0-rc6] - 2017-06-22

### Changed
- Improved logging for annotation scanning
- Add component to audit interceptor so that audit messages can distinguish between components even
  when they are deployed in a single WAR.

## [2.0.0-rc5] - 2017-06-20

### Changed
- Include base URI in class name for generated JMS listeners. This ensures they are unique, but any project that overrides the generated
  class will need to change the class name of their override to match.

## [2.0.0-rc4] - 2017-06-19

### Fixed
- Aggregate snapshot service was pulling in Liquibase due to an incorrect dependency scope

## [2.0.0-rc3] - 2017-06-16

### Changed
- Logging dependencies tidied up - all logging implementations excluded from dependencies and tests use new test utils modules for logging

### Removed
- Precondition class marked as deprecated - will be removed in 3.0.0 unless a differen tuse case is found for it

## [2.0.0-rc2] - 2017-06-06

### Changed
- Interceptor chain now adds the component name to the context so it can be used by the access control interceptor or anything else that needs it

### Removed
- Access control Provider annotation and annotation scanning; this functionality has moved to the access control library

## [2.0.0-rc1] - 2017-05-31

### Changed
- Refactor all framework components that are not internal so that they are provided as interfaces
  via new Framework API modules
- Rework interceptor chain so that it is specific to a service component, by allowing each component
  to provide an interceptor chain definition rather than using annotation scanning
- Upgrade to use framework parent POM [1.3.0](https://github.com/CJSCommonPlatform/maven-framework-parent-pom/releases/tag/release-1.3.0)

### Removed
- Support for default sender destinations removed; senders now always require messaging clients to
  be provided, typically by generating one from the destination RAML.

### Fixed
- Test cases for random ZonedDateTime generators and added logging to show more info when they fail
- Javadoc errors

### Added
- Script for building dependencies locally
- Support for generating and discovering direct adapters, if a message destination exists locally
  a service component in the same application

## [1.7.1] - 2017-05-16

### Added
- Utility for browsing and deleting DLQ messages, backported from separate test utils library
- Support for adding additional fields when building metadata

## [1.7.0] - 2017-05-16

### Added
- Add test event log repository to the test-utils-core module

## [1.6.0] - 2017-05-05

### Added
- Support for PDF generation in Alfresco interface

## [1.5.2] - 2017-04-07

###
- Service names with hyphens were also breaking other adapters and clients

## [1.5.1] - 2017-04-05

### Fixed
- Event listeners for services with a hyphen in the name generated invalid class names

## [1.5.0] - 2017-03-30

### Added
- MultipartRestClient in test-utils: client for multipart file uploads
- LiquibaseDatabaseBootstrapper in test-utils: bootstraps a database using your liquibase scripts
- Dependency on utilities-core
- Ability for multipart endpoint to handle multiple files
- Generators for generating multipart endpoints from RAML

### Fixed
- Generate random ZonedDateTime in different time zones and provide option to generate in UTC specific timezone

### Removed
- Duplicate classes that are in utilities-core from the framework
- Configuration classes that are now in utilities-core

### Updated
- Use File Service version 1.8.0
- Use Utilities version 1.6.0
- JsonEnvelopePayloadMatcher to support matching of JsonValue NULL payloads

## [1.4.3] - 2017-03-30

### Fixed
- Duplicate method names in REST client generator, fixed by making method name generation use more things
- Concurrently issue in event stream appends; optimistic locking did not kick in when it should

## [1.4.2] - 2017-03-08

### Fixed
- Uplift Resteasy dependency versions and changed to provided scope
- Allow JNDI values to fall back to globals
- Performance fix to internal optimistic locking failure retries

## [1.4.1] - 2017-02-13

### Fixed
- ObjectMapper truncation of converted ZoneDateTimes when milliseconds part ends with zero
- Ignore non vendor-specific media types while generating clients

## [1.4.0] - 2017-02-02

### Added
- JsonEnveloperBuilder in test-utils-core to replace the deprecated builer in DefaultJsonEnvelope.
- Generator support for CustomAdapter and CustomServiceComponent annotations

### Fixed
- Metadata causation being ignored in the Rest Adapter

### Deprecated
- Deprecated the DefaultJsonEnvelope builder methods in favour of a test utils version.

## [1.3.0] - 2017-01-26

### Fixed
- Handle ACCEPTED(202) response type set in raml for asynchronous REST endpoints
- Fix of unclosed connections in MessageConsumerClient
- Log warning if generated rest adapter already exists

## [1.2.0] - 2017-01-19

### Added
- No wait retrieve method to MessageConsumerClient
- No close method to MessageConsumerClient

### Fixed
- wrong version of apache bean utils pulled in by open ejb core

## [1.1.0] - 2017-01-19

### Fixed
- Fix logging filter metadata bug

### Added
- Immediate retries to RetryInterceptor, defaults to 3 before applying wait period between retries
- Support for Http Methods DELETE, PATCH, POST and PUT.  REST Adaptor and REST Client generators now
  support RAML that contains asynchronous DELETE, PATCH and PUT, and synchronous PATCH, POST and PUT.
- Support for matchers in TypeCheck class.

### Changed
- Optimistic lock log message changed from warn to debug.
- Move default port provider to common module
- Add ConflictedResourceException for 409 responses
- Common-bom version to 1.6.0

## [1.0.1] - 2016-12-23

### Fixed
- Logging filter was breaking if a message payload contained the string __metadata_ to avoid having
  to parse the JSON; fixed so that it only looks for top level a top level _metadata field.

## [1.0.0] - 2016-12-16

### Added
- Logging request data is set in the SLF4J mapped diagnostic context (MDC) and can be added to the
  log output by setting %X{requestData} in the logger pattern
- Support for managing optimistic lock retry for event log, when using the PostgreSQL database.
  Default is to retry forever.
- ZonedDateTimeGenerator to generate random future or past ZonedDateTimes

### Changed
- Improve ResponsePayloadMatcher to support string matchers on response payload
- Upgraded ObjectMapper to allow single arg constructors in Object serialization
- Aggregate snapshot repository enabled by default. This requires the `aggregate-snapshot-repository-liquibase`
  schema to have been applied to the event store database, which makes this release backwards incompatible
- Event timestamps now added to private events automatically and stored in the event store as part
  of the metadata and in a separate field. This requires the latest `event-repository-liquibase`
  schema to be applied to the event store database, which makes this release backwards incompatible

### Removed
- DateTimeProvider after two months deprecation. Use Clock/UtcClock instead.

### Fixed
- JsonSchemaValidationMatcher to look for json schema in correct location
- JSON schema validation of date-time format fixed by using a forked version of the JSON schema
  validator library
- JsonSchemaValidationMatcher to fallback to raml maven dependency if not on json classpath

## [0.35.0] - 2016-11-24
### Added
- File, file-api and file-alfresco modules
- File service interface
- Alfresco file service implementation

### Fixed
- Refactor random generators for string, uri and email

## [0.34.0] - 2016-11-16

### Added
- Stream of streams event retrieval
- Proxy support to Rest Client
- JsonObjects toJsonArray method

### Changed
- Improve BigDecimalGenerator to cover both positive and negative range
- Improve DoubleGenerator to cover the bounds of double
- TypeCheck class to provide better feedback on failure
- Parent pom to 1.2.0, common bom to 1.4.0 and raml-plugin to 1.3.0

### Fixed
- JDBC Repository resource close ordering
- Test cases related to random date generation
- ValueGenerator to randomly pick items from a given pool and renamed the class to ItemPicker

## [0.33.0] - 2016-10-31

### Added
- Support for RestClient to use proxy details from environment properties
- Matchers for matching handler and handler class methods, annotations and pass through process type (Sender or Requester)
- Empty stream matching to EventStreamMatcher
- toJsonArray utility function

### Changed
- Improved event stream processing

## [0.32.0] - 2016-10-24

### Added
- JsonEnvelope.asJsonObject() for simple conversion of the entire envelope to a JsonObject.
- EventStreamMatcher to match stream of JsonEnvelopes appended
- RestPoller. A polling REST client utility for integration tests
- Mechanism for taking snapshots of aggregates, disabled by default. To enable, add a dependency on
  the `aggregate-snapshot-service` module. Requires the `aggregate-snapshot-repository-liquibase`
  schema to be applied to the event store.
- JSON schema matching support in the JsonEnvelopeMatcher
- Added new module 'rest-core'
- Added 'rest-client-core' as a standard dependency for event-processor'
- Added 'hamcrest-date' as a standard dependency for 'test-utils-core'

### Changed
- JsonEnvelopeMetadataMatcher to allow matching with JSON paths
- Deprecated PollingRestClient in favour of the new RestPoller

### Fixed
- RestProcessor now allows metadata from payload to be merged with headers instead of being
  overwritten
- Removed unwanted dependency on the RAML parser within the REST adapter so that adding the REST client to event processors does not break the application

## 0.31.0 - 2016-10-24

- Failed release; do not use

## [0.30.0] - 2016-10-11

### Fixed
- Event buffer connection held open after exception in event listener
- RestClientProcessor tests clashing using common 8080 port
- JMS listeners for event topics did not use shared subscriptions. Fixing this allows multiple
  instances to run. Each message will be consumed only once across a cluster.

### Added
- Hamcrest Matchers for asserting JsonEnvelopes contained within either Streams or Lists
- New Clock interface to replace DateTimeProvider
- EnumPicker in random generators

### Changed
- DateTimeProvider is now deprecated - use Clock instead
- JsonEnvelopeBuilder is now deprecated - use DefaultJsonEnvelope.envelope() instead
- Extend DefaultJsonEnvelope.Builder to accept JsonObject as part of the payload

### Removed
- Unused JdbcConnectionProvider utility

## [0.29.0] - 2016-09-30

### Fixed
- 'Response is closed' bug in PollingRequestClient

### Added
- ZonedDateTimes methods to convert between ZDT and SQL timestamps
- LocalDate conversion functions
- EnveloperFactory method to create a Enveloper with a list of Event classes registered
- EventStreamMockHelper that provides a method to verify and return the Stream argument from a call
  to the EventStream append method
- DateProvider to allow easy mocking of date creating for testing
- Random generators and TypeCheck class for type-based testing
- Metrics per action name

### Changed
- Event Store to include a 'date_created' timestamp field - added to the DB schema but not yet
  enabled in code

## [0.28.0] - 2016-09-21

### Fixed
- EventBufferInterceptor container discovery

## [0.27.0] - 2016-09-20
### Added
- JsonSchemaValidationMatcher class to validate json content against a schema
- PollingRequestClient class as a new implementation of the HttpResponsePoller

### Changed
- Moved EventBufferInterceptor and EventFilterInterceptor to event-listener component
- Added withHeaders method to HttpResponsePoller

### Fixed
- BaseTransactionalTest to cleanup with rollback

### Deprecated
- HttpResponsePoller, replaced with PollingRestClient

## [0.26.0] - 2016-09-20
- Failed release; do not use

## [0.25.0] - 2016-09-12
### Added
- sender.sendAsAdmin() method

### Fixed
- NPE JsonSenderWrapper

## [0.24.0] - 2016-09-08

### Added
- Configurable JNDI Auditing blacklist regex of action names in AuditingService
- Expose component metrics via Rest and JMX
- TestJdbcConnectionProvider: for getting hard out of container connections
  to the event and view stores
- DatabaseCleaner: allows easy clearing of database tables for integration tests


## [0.23.0] - 2016-09-01

### Added
- persistence-jdbc to the framework bom


## [0.22.0] - 2016-08-31

### Added
- Add JDBC Connection classes for easy access to event store and view store databases

### Fixed
- Fixed message producer client to use a system property to override the queue url

## [0.21.0] - 2016-08-30

### Added
- Add json object value matching to HttpResponsePoller utility
- Add a 'Request as Admin' request to the requester

### Fixed
- HttpResponsePoller conditional poll fixed

## [0.19.0] - 2016-08-26

### Added
- Dispatcher interceptor integration. Interceptors are chained between the adapter and the dispatcher
  according to a priority setting.  Interceptors implement the Interceptor interface and are registered
  at startup.  
  Implemented interceptors: Event Buffer Interceptor, Access Control Interceptor
- Event Listener Filter
- Additional features to the HttpResponsePoller utility

### Fixed
- Remote Client unable to POST to REST end point with media type that is different to action name
- SenderProducer support for @FrameworkComponent annotated Senders


## [0.18.0] - 2016-08-22

### Added
- test-utils-persistence to the framework bom

### Fixed
- CORS response header mismatch
- JMS Message Producer test-util connection closing issue


## [0.17.0] - 2016-08-19

### Fixed
- Travis build file settings
- Javadoc build issues


## [0.16.0] - 2016-08-18

### Added
- MessageProducerClient in test-utils for easy integration testing of sending messages
- UuidStringMatcher: A Hamcrest matcher for asserting that a string is a valid UUID
- EnvelopeFactory: for creating a simple JsonEnvelope for testing

### Changed
- Updated to use DeltaSpike container managed persistence and transaction

### Removed
- Remove asynchronous and synchronous differences from Dispatcher


## [0.15.0] - 2016-08-11

### Added
- Initial implementation of event ordering buffer for event listeners
- Add a simple Audit Client
- Add a toDebugStringPrettyPrinted() method that returns the JsonEnvelope as JSON

### Changed
- Move the logic of JsonEnvelopeLoggerHelper to the toString() method of JsonEnvelope
- Move EnveloperFactory to test utils


## [0.14.0] - 2016-08-08

### Added
- Add a match all and do nothing EventMatcher to the EventSwitcher. This will ignore all other events.
  Example:
```
match(event).with(
    when(SomethingAdded.class).apply(x -> id = x.getId()),
    otherwiseDoNothing());
```
- Added test utility classes for logger producer, test messaging client and other http utilities.

### Changed
- Removed schema validation for requests without a payload (actions without schema/example specified in raml and denoted with !!null).

Example (Two actions, the second has no payload):
```
application/vnd.people.modified-user+json:
    schema: !include json/schema/people.modified-user.json
    example: !include json/update-user.json
application/vnd.people.link-user+json: !!null
```

## [0.13.0] - 2016-07-28

### Added
- Service component passthrough test utility; test Command API, Command Controller, Query API and
  Query Controller as passthrough services
- Support for listening to all events on a topic or queue

### Fixed
- Causation HTTP header not sent by the REST client

### Changed
- Removed limitation on messaging RAML resources to allow any queue or topic name

## [0.12.3] - 2016-07-19

### Fixed
- 403 response from REST calls caused 500 to be returned
- Stream order not guaranteed when retrieving events from the event store

## [0.12.0] - 2016-07-14

### Changed
- Use new parent POM and common POM projects

### Fixed
- Prevent access control triggering for remote handlers
- Ignore GET resources when generating JMS adapters
- Support for Event API components in RAML

### Removed
- Action mapper annotation now always required in REST RAML; it is no longer possible to disable the
  action mapper system

## [0.11.0] - 2016-07-08

### Added
- Access control violations now return 403 forbidden response
- Support for Event API components in RAML

### Fixed
- Access control provider scanning and bean injection
- Event processor and JEE dependencies were incorrect
- Component module dependencies cleaned up and made consistent

## [0.10.1] - 2016-07-05

### Fixed

- Set framework BOM to POM packaging

## [0.10.0] - 2016-07-05

### Added

- Support for generating messaging clients from RAML
- Added EVENT_API service component type
- Support for simple access control with a default implementation that allows all requests
- New ZonedDateTimes utility class for converting JSON strings to UTC date times
- New JsonEnvelopeBuilder test utility class for building envelopes
- Bill of materials (BOM) for easier framework module dependency management in other Maven projects

### Changed

- Object mapper configured to exclude nulls from JSON
- Ensure dates are stored and retrieved in UTC format
- Refactor DispatcherProvider into component parts
- Updated USER_ID constant in response to change by IDAM
- Updated COMMAND_API service component type to an http default input

## [0.9.0] - 2016-06-15

### Changed

- Messaging adapter generator now uses Java Poet for code generation instead of a template

### Fixed

- Fix RAML action mapping description to allow other description text surrounding the mapping
- Fix action mapper to support media types with different character sets

## [0.8.12] - 2016-06-13

### Added

- Support for [types](https://github.com/raml-org/raml-spec/blob/master/versions/raml-08/raml-08.md#type) on query parameters in the REST adapter generator
- Initial [action mapping](https://github.com/CJSCommonPlatform/microservice_framework/wiki/User-Guide#rest-adapter-generator) support for the REST adapter generator,
  turned off by default

### Fixed

- Fix media type handling in the test utilities REST client

## [0.8.11] - 2016-06-07

### Changed

- Ensure Jackson always adds a timezone when marshalling timestamps
- Allow JAX-RS providers to be overridden in generated REST adapters

### Fixed
- Do not change port on REST requests to service components within the current service

## [0.8.10] - 2016-06-03

### Added

- Configuration option to control REST client port via a system property
- Add user id, session id and correlation id to REST headers for remote calls
- JSON schema validation error [logging](https://github.com/CJSCommonPlatform/microservice_framework/wiki/User-Guide#logging)

## [0.8.9] - 2016-05-31

### Changed

- Allow senders to be annotated at the field level

### Added

- Add ListToJsonArrayConverter

## [0.8.8] - 2016-05-31

### Added

- Requester injection for non-handler classes
- Skip generation flag for RAML plugin
- Metadata handling for REST client queries
- POST support for REST clients
- Persistence module and example for Deltaspike integration testing

## [0.8.7] - 2016-05-26

### Added

- CORS filter

## [0.8.6] - 2016-05-26

### Added

- Message trace [logging](https://github.com/CJSCommonPlatform/microservice_framework/wiki/User-Guide#logging)
- JEE integration test support
- REST client test-utils module
- Version now supplied in event metadata

## [0.8.5] - 2016-05-23

### Changed

- Revert to consistently use Jackson 2.6.4

## [0.8.4] - 2016-05-23

### Changed

- Use Jackson 2.7.4

## [0.8.3] - 2016-05-23

### Changed

- Relax event type validation to accept plural to ease context migration to new framework

## [0.8.2] - 2016-05-19

### Added

- Support for remote service invocation

## [0.8.1] - 2016-05-12

### Added

- Add annotation support for properties
- Add JSON schema validation support
- Support 404 response
- Optional query parameter support
- Support for endpoint exclusion in RAML rest generator
- Add aggregate service and helper functions

### Changed

- Convert REST adapter generator to use Java Poet
- Disable WRITE_DATES_AS_TIMESTAMPS in Jackson

### Fixed

- Fix generator duplicate class detection for multi-platform support

## [0.8.0] - 2016-04-22

### Added

- Initial release with basic dispatcher, handler and adapter generation

[Unreleased]: https://github.com/CJSCommonPlatform/microservice_framework/compare/release-2.2.1...HEAD
[2.2.1]: https://github.com/CJSCommonPlatform/microservice_framework/compare/release-2.2.0...release-2.2.1
[2.2.0]: https://github.com/CJSCommonPlatform/microservice_framework/compare/release-2.1.0...release-2.2.0
[2.1.0]: https://github.com/CJSCommonPlatform/microservice_framework/compare/release-2.0.0...release-2.1.0
[2.1.0]: https://github.com/CJSCommonPlatform/microservice_framework/compare/release-2.0.0...release-2.1.0
[2.0.0]: https://github.com/CJSCommonPlatform/microservice_framework/compare/release-1.7.0...release-2.0.0
[2.0.0-rc8]: https://github.com/CJSCommonPlatform/microservice_framework/compare/release-2.0.0-rc7...release-2.0.0-rc8
[2.0.0-rc7]: https://github.com/CJSCommonPlatform/microservice_framework/compare/release-2.0.0-rc6...release-2.0.0-rc7
[2.0.0-rc6]: https://github.com/CJSCommonPlatform/microservice_framework/compare/release-2.0.0-rc5...release-2.0.0-rc6
[2.0.0-rc5]: https://github.com/CJSCommonPlatform/microservice_framework/compare/release-2.0.0-rc4...release-2.0.0-rc5
[2.0.0-rc4]: https://github.com/CJSCommonPlatform/microservice_framework/compare/release-2.0.0-rc3...release-2.0.0-rc4
[2.0.0-rc3]: https://github.com/CJSCommonPlatform/microservice_framework/compare/release-2.0.0-rc2...release-2.0.0-rc3
[2.0.0-rc2]: https://github.com/CJSCommonPlatform/microservice_framework/compare/release-2.0.0-rc1...release-2.0.0-rc2
[2.0.0-rc1]: https://github.com/CJSCommonPlatform/microservice_framework/compare/release-1.7.0...release-2.0.0-rc1
[1.7.1]: https://github.com/CJSCommonPlatform/microservice_framework/compare/release-1.7.0...release-1.7.1
[1.7.0]: https://github.com/CJSCommonPlatform/microservice_framework/compare/release-1.6.0...release-1.7.0
[1.6.0]: https://github.com/CJSCommonPlatform/microservice_framework/compare/release-1.5.0...release-1.6.0
[1.5.1]: https://github.com/CJSCommonPlatform/microservice_framework/compare/release-1.5.0...release-1.5.1
[1.5.0]: https://github.com/CJSCommonPlatform/microservice_framework/compare/release-1.4.0...release-1.5.0
[1.4.3]: https://github.com/CJSCommonPlatform/microservice_framework/compare/release-1.4.2...release-1.4.3
[1.4.2]: https://github.com/CJSCommonPlatform/microservice_framework/compare/release-1.4.1...release-1.4.2
[1.4.1]: https://github.com/CJSCommonPlatform/microservice_framework/compare/release-1.4.0...release-1.4.1
[1.4.0]: https://github.com/CJSCommonPlatform/microservice_framework/compare/release-1.3.0...release-1.4.0
[1.3.0]: https://github.com/CJSCommonPlatform/microservice_framework/compare/release-1.2.0...release-1.3.0
[1.2.0]: https://github.com/CJSCommonPlatform/microservice_framework/compare/release-1.1.0...release-1.2.0
[1.1.0]: https://github.com/CJSCommonPlatform/microservice_framework/compare/release-1.0.1...release-1.1.0
[1.0.1]: https://github.com/CJSCommonPlatform/microservice_framework/compare/release-1.0.0...release-1.0.1
[1.0.0]: https://github.com/CJSCommonPlatform/microservice_framework/compare/release-0.33.0...release-1.0.0
[0.33.0]: https://github.com/CJSCommonPlatform/microservice_framework/compare/release-0.32.0...release-0.33.0
[0.32.0]: https://github.com/CJSCommonPlatform/microservice_framework/compare/release-0.30.0...release-0.32.0
[0.30.0]: https://github.com/CJSCommonPlatform/microservice_framework/compare/release-0.29.0...release-0.30.0
[0.29.0]: https://github.com/CJSCommonPlatform/microservice_framework/compare/release-0.28.0...release-0.29.0
[0.28.0]: https://github.com/CJSCommonPlatform/microservice_framework/compare/release-0.27.0...release-0.28.0
[0.27.0]: https://github.com/CJSCommonPlatform/microservice_framework/compare/release-0.26.0...release-0.27.0
[0.26.0]: https://github.com/CJSCommonPlatform/microservice_framework/compare/release-0.25.0...release-0.26.0
[0.25.0]: https://github.com/CJSCommonPlatform/microservice_framework/compare/release-0.24.0...release-0.25.0
[0.24.0]: https://github.com/CJSCommonPlatform/microservice_framework/compare/release-0.23.0...release-0.24.0
[0.23.0]: https://github.com/CJSCommonPlatform/microservice_framework/compare/release-0.22.0...release-0.23.0
[0.22.0]: https://github.com/CJSCommonPlatform/microservice_framework/compare/release-0.21.0...release-0.22.0
[0.21.0]: https://github.com/CJSCommonPlatform/microservice_framework/compare/release-0.19.0...release-0.21.0
[0.19.0]: https://github.com/CJSCommonPlatform/microservice_framework/compare/release-0.18.0...release-0.19.0
[0.18.0]: https://github.com/CJSCommonPlatform/microservice_framework/compare/release-0.17.0...release-0.18.0
[0.17.0]: https://github.com/CJSCommonPlatform/microservice_framework/compare/release-0.16.0...release-0.17.0
[0.16.0]: https://github.com/CJSCommonPlatform/microservice_framework/compare/release-0.15.0...release-0.16.0
[0.15.0]: https://github.com/CJSCommonPlatform/microservice_framework/compare/release-0.14.0...release-0.15.0
[0.14.0]: https://github.com/CJSCommonPlatform/microservice_framework/compare/release-0.13.0...release-0.14.0
[0.13.0]: https://github.com/CJSCommonPlatform/microservice_framework/compare/release-0.12.0...release-0.13.0
[0.12.0]: https://github.com/CJSCommonPlatform/microservice_framework/compare/release-0.11.0...release-0.12.0
[0.11.0]: https://github.com/CJSCommonPlatform/microservice_framework/compare/release-0.10.1...release-0.11.0
[0.10.1]: https://github.com/CJSCommonPlatform/microservice_framework/compare/release-0.10.0...release-0.10.1
[0.10.0]: https://github.com/CJSCommonPlatform/microservice_framework/compare/release-0.9.0...release-0.10.0
[0.9.0]: https://github.com/CJSCommonPlatform/microservice_framework/compare/release-0.8.12...release-0.9.0
[0.8.12]: https://github.com/CJSCommonPlatform/microservice_framework/compare/release-0.8.11...release-0.8.12
[0.8.11]: https://github.com/CJSCommonPlatform/microservice_framework/compare/release-0.8.10...release-0.8.11
[0.8.10]: https://github.com/CJSCommonPlatform/microservice_framework/compare/release-0.8.9...release-0.8.10
[0.8.9]: https://github.com/CJSCommonPlatform/microservice_framework/compare/release-0.8.8...release-0.8.9
[0.8.8]: https://github.com/CJSCommonPlatform/microservice_framework/compare/release-0.8.7...release-0.8.8
[0.8.7]: https://github.com/CJSCommonPlatform/microservice_framework/compare/release-0.8.6...release-0.8.7
[0.8.6]: https://github.com/CJSCommonPlatform/microservice_framework/compare/release-0.8.5...release-0.8.6
[0.8.5]: https://github.com/CJSCommonPlatform/microservice_framework/compare/release-0.8.4...release-0.8.5
[0.8.4]: https://github.com/CJSCommonPlatform/microservice_framework/compare/release-0.8.3...release-0.8.4
[0.8.3]: https://github.com/CJSCommonPlatform/microservice_framework/compare/release-0.8.2...release-0.8.3
[0.8.2]: https://github.com/CJSCommonPlatform/microservice_framework/compare/release-0.8.1...release-0.8.2
[0.8.1]: https://github.com/CJSCommonPlatform/microservice_framework/compare/release-0.8.0...release-0.8.1
[0.8.0]: https://github.com/CJSCommonPlatform/microservice_framework/commits/release-0.8.0
