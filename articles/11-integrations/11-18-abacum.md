# Abacum Integration

Abacum is a financial planning and analysis (FP&A) platform that helps finance teams build budgets, create forecasts, and generate collaborative financial reports. Light's Abacum integration synchronizes your actual financial data with Abacum, enabling real-time budget-to-actual analysis and streamlined financial planning.

[Open in Light →](https://app.light.inc/settings/integrations)

## Integration overview

The Abacum integration enables:

- **Actuals sync**: Automatically push actual financial data from Light to Abacum for comparison against budgets and forecasts
- **Chart of accounts sync**: Keep your account structure consistent between Light and Abacum
- **Dimension sync**: Synchronize custom properties (departments, projects, cost centers) for consistent reporting
- **Multi-entity support**: Sync data across multiple entities for consolidated planning
- **Real-time updates**: Keep Abacum forecasts current with the latest actual performance

This eliminates manual data exports and ensures your FP&A team always works with accurate, up-to-date numbers.

## Setting up the Abacum integration

To connect Abacum:

1. Navigate to **Settings (gear icon) > Integrations > Abacum**
2. Click **Connect**
3. You're redirected to Abacum to authorize
4. Enter your Abacum credentials
5. Review the permissions Light is requesting
6. Click **Authorize**
7. Light confirms the connection is active

Next, configure what data to sync.

## Configuring actuals sync

Define how financial data flows to Abacum:

1. Navigate to **Settings > Integrations > Abacum > Data Mapping**
2. Select **Sync Actuals**: Toggle on
3. Configure data scope:
   - **Entities**: Select which entities to sync (all or specific ones)
   - **Account types**: Choose which account types to include (revenue, expenses, assets, liabilities)
   - **Date range**: Specify historical data to sync initially
4. Configure sync frequency:
   - **Daily**: Sync once per day (recommended for most organizations)
   - **Hourly**: Sync every hour for real-time analysis
   - **Manual**: Only sync when triggered
5. Save configuration

Light validates the connection and performs an initial sync.

## Chart of accounts mapping

Ensure your accounts align between systems:

1. Navigate to **Settings > Integrations > Abacum > Account Mapping**
2. Light displays your chart of accounts alongside Abacum accounts
3. For each Light account, select the corresponding Abacum account:
   - **Light Revenue Account** → **Abacum Revenue Category**
   - **Light Expense Account** → **Abacum Expense Category**
   - **Light Asset Account** → **Abacum Balance Sheet Item**
4. Use **Auto-map** to automatically match accounts with similar names
5. Review and adjust any mismatches
6. Save mappings

Consistent account mapping ensures accurate budget-to-actual comparisons.

> Tip: If you add new accounts in Light, remember to update the Abacum mapping to include them.

## Dimension and custom property sync

Synchronize reporting dimensions for consistent analysis:

1. Navigate to **Settings > Integrations > Abacum > Dimension Mapping**
2. Map Light custom properties to Abacum dimensions:
   - **Light Department** → **Abacum Department**
   - **Light Project** → **Abacum Project**
   - **Light Cost Center** → **Abacum Cost Center**
   - **Light Region** → **Abacum Geography**
3. Configure dimension value mappings if names differ between systems
4. Save mappings

This enables granular budget-to-actual analysis by department, project, or any other dimension.

## Multi-entity sync

For organizations with multiple entities:

1. Navigate to **Settings > Integrations > Abacum > Entity Settings**
2. Select which Light entities to sync:
   - Toggle on each entity you want to include
   - Map each Light entity to the corresponding Abacum entity
3. Configure consolidation settings:
   - **Sync individual entities**: Push data for each entity separately
   - **Sync consolidated**: Push consolidated group data
   - **Sync both**: Push both individual and consolidated data
4. Save configuration

This supports complex organizational structures and consolidated planning.

## What data syncs to Abacum

Light sends the following data to Abacum:

**Financial data**:
- Trial balance by period
- Profit and loss actuals
- Balance sheet actuals
- Cash flow data

**Dimensional data**:
- Department-level actuals
- Project-level actuals
- Cost center actuals
- Any custom property values

**Metadata**:
- Account names and hierarchies
- Entity structure
- Period definitions

Abacum uses this data to populate actuals columns in budgets and forecasts.

## Real-time budget variance analysis

With the integration active, your FP&A team can:

1. Create budgets and forecasts in Abacum
2. Light automatically syncs actual performance
3. Abacum displays real-time variances:
   - Budget vs. actual
   - Forecast vs. actual
   - Prior period vs. current period
4. Drill down into variances by account, department, or project
5. Adjust forecasts based on actual trends

This enables proactive financial management rather than reactive reporting.

## Sync frequency and timing

Configure when data syncs:

1. Navigate to **Settings > Integrations > Abacum > Sync Settings**
2. Select frequency:
   - **Daily at close**: Sync after daily close process (recommended)
   - **Hourly**: Sync every hour for near-real-time data
   - **On-demand**: Manual sync only
3. Select time zone for scheduled syncs
4. Optionally set a sync delay (e.g., sync at 6 AM after nightly processes complete)
5. Save

Daily sync after close ensures Abacum always has complete, reconciled data.

## Monitoring sync status

Track integration activity:

1. Navigate to **Settings > Integrations > Abacum > Sync History**
2. View past syncs:
   - Date/time of sync
   - Number of records synced
   - Data volume transferred
   - Status (success, partial, failed)
3. Click any sync to see details:
   - Which accounts were synced
   - Which periods were updated
   - Any errors or warnings

This helps identify and resolve issues quickly.

## Manual sync trigger

Manually trigger a sync when needed:

1. Navigate to **Settings (gear icon) > Integrations > Abacum**
2. Click **Sync Now**
3. Light immediately pushes current data to Abacum
4. You see a summary of what was synced

Useful after posting significant journal entries or closing a period.

## Handling sync errors

If syncs fail:

1. Check the error message in sync history
2. Common errors:
   - **Unmapped account**: A Light account isn't mapped to Abacum
   - **Invalid dimension value**: A custom property value doesn't exist in Abacum
   - **Authentication expired**: Re-authorize the Abacum connection
   - **Rate limit exceeded**: Too many syncs in a short period
3. Fix the issue (update mappings, re-authorize, etc.)
4. Retry the sync

Light provides detailed error messages to help diagnose issues.

## Data security and privacy

The Abacum integration follows security best practices:

- **OAuth authentication**: Credentials are never stored in Light
- **Encrypted transfer**: All data is encrypted in transit
- **Scoped access**: Light only requests necessary permissions
- **Audit trail**: All sync activity is logged

You can revoke access at any time from either Light or Abacum.

## Disconnecting the integration

To disconnect Abacum:

1. Navigate to **Settings (gear icon) > Integrations > Abacum**
2. Click **Disconnect**
3. Confirm the disconnection
4. Light stops syncing data to Abacum

Historical data already synced to Abacum remains there until deleted in Abacum.

## Troubleshooting common issues

**Data not appearing in Abacum**: Verify account mappings are complete, check sync history for errors, ensure the period is open in Abacum.

**Incorrect amounts**: Check account mapping, verify currency conversion settings, review period alignment.

**Missing dimensions**: Update dimension mappings in integration settings, ensure dimension values exist in both systems.

**Connection failed**: Re-authorize the integration, verify your Abacum account has API access enabled.

**Stale data**: Check sync frequency settings, manually trigger a sync, verify scheduled syncs are running.

## Related articles

- [Integrations overview](11-1-integrations-overview.md)
- [Budget scenarios and overview](../10-reporting/10-10-budget-scenarios.md)
- [Profit and loss](../10-reporting/10-3-profit-loss.md)
- [Multi-entity consolidation](../10-reporting/10-7-multi-entity-consolidation.md)
- [Custom properties setup](../02-organization-setup/2-3-custom-properties.md)
