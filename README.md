# Roblox Engine API

Roblox provides a suite of developer APIs for building experiences on the Roblox platform. The Engine API documents all classes, data types, enumerations, functions, events, callbacks, and properties for in-experience scripting in Luau. The Open Cloud REST API provides external programmatic access to Roblox platform resources including experiences, places, data stores, users, groups, assets, messaging, and more. In March 2026, Roblox launched new unified Open Cloud reference documentation.

**Website:** [https://www.roblox.com](https://www.roblox.com)

**Developer Portal:** [https://create.roblox.com](https://create.roblox.com)

**Developer Forum:** [https://devforum.roblox.com](https://devforum.roblox.com)

## APIs

### Roblox Engine API

The Roblox Engine API documents all classes, data types, enumerations, global functions, variables, and libraries available when scripting Roblox experiences in Luau.

- **Documentation:** [https://create.roblox.com/docs/reference/engine](https://create.roblox.com/docs/reference/engine)

### Roblox Open Cloud API

The Roblox Open Cloud API is a REST API providing external programmatic access to Roblox platform resources. Authentication uses API keys scoped to specific resources via the `x-api-key` header.

- **Base URL:** `https://apis.roblox.com`
- **Authentication:** API Key (`x-api-key` header)
- **Documentation:** [https://create.roblox.com/docs/cloud/reference](https://create.roblox.com/docs/cloud/reference)
- **OpenAPI Spec:** [https://create.roblox.com/docs/cloud/reference/openapi](https://create.roblox.com/docs/cloud/reference/openapi)

#### Key Endpoints

| Method | Path | Description |
|--------|------|-------------|
| GET | `/cloud/v2/universes/{universeId}` | Get experience details |
| PATCH | `/cloud/v2/universes/{universeId}` | Update experience settings |
| POST | `/cloud/v2/universes/{universeId}:restart-servers` | Restart all game servers |
| GET | `/cloud/v2/universes/{universeId}/places/{placeId}` | Get place details |
| POST | `/universes/v1/{universeId}/places/{placeId}/versions` | Publish a place |
| GET | `/datastores/v1/universes/{universeId}/standard-datastores` | List data stores |
| POST | `/datastores/v1/universes/.../entries/entry` | Set data store entry |
| POST | `/messaging-service/v1/universes/{universeId}/topics/{topic}` | Publish message |
| GET | `/cloud/v2/users/{userId}` | Get user information |
| GET | `/cloud/v2/groups/{groupId}` | Get group information |
| PATCH | `/cloud/v2/universes/{universeId}/user-restrictions/{userId}` | Ban/unban player |

## Artifacts

### OpenAPI Specifications

| Spec | Description |
|------|-------------|
| [openapi/roblox-open-cloud-openapi.yml](openapi/roblox-open-cloud-openapi.yml) | Roblox Open Cloud API — universes, places, data stores, messaging, users, groups |

### Spectral Rules

| Ruleset | Description |
|---------|-------------|
| [rules/roblox-open-cloud-rules.yml](rules/roblox-open-cloud-rules.yml) | Roblox Open Cloud linting rules enforcing x-api-key auth and camelCase conventions |

### Capabilities

| Capability | Description |
|------------|-------------|
| [capabilities/experience-management.yaml](capabilities/experience-management.yaml) | Unified workflow for Roblox experience management including moderation and data stores |
| [capabilities/shared/open-cloud.yaml](capabilities/shared/open-cloud.yaml) | Shared Open Cloud API consumed definition |

### JSON Schemas

| Schema | Description |
|--------|-------------|
| [json-schema/roblox-universe-schema.json](json-schema/roblox-universe-schema.json) | Roblox universe (experience) resource |
| [json-schema/roblox-user-schema.json](json-schema/roblox-user-schema.json) | Roblox user resource from Open Cloud |

### JSON Structure

| Structure | Description |
|-----------|-------------|
| [json-structure/roblox-universe-structure.json](json-structure/roblox-universe-structure.json) | Field documentation for the universe object |

### JSON-LD Context

| Context | Description |
|---------|-------------|
| [json-ld/roblox-engine-api-context.jsonld](json-ld/roblox-engine-api-context.jsonld) | Linked data context mapping Roblox platform terms to schema.org |

### Examples

| Example | Description |
|---------|-------------|
| [examples/roblox-get-universe-example.json](examples/roblox-get-universe-example.json) | Get universe details with request/response |
| [examples/roblox-set-datastore-entry-example.json](examples/roblox-set-datastore-entry-example.json) | Set a data store entry with player data |

### Vocabulary

| Vocabulary | Description |
|------------|-------------|
| [vocabulary/roblox-engine-api-vocabulary.yml](vocabulary/roblox-engine-api-vocabulary.yml) | Roblox platform terms including Universe, DataStore, Luau, OpenCloud, UserRestriction |

## Tags

Gaming, Game Development, Metaverse, Roblox, Open Cloud

## Maintainers

**FN:** Kin Lane

**Email:** kin@apievangelist.com
