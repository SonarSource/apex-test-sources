# IT Apex sources

## Source code origin
```bash
cd projects
git clone git@github.com:ipavlic/apex-lambda.git
git clone git@github.com:financialforcedev/apex-mdapi.git
git clone git@github.com:afawcett/apex-toolingapi.git
git clone git@github.com:mbotos/Automated-Testing-for-Force.com.git
git clone git@github.com:SalesforceFoundation/Batch-Entry-for-Salesforce.com.git
git clone git@github.com:SalesforceFoundation/Cumulus.git
git clone git@github.com:forcedotcom/CustomMetadataLoader.git
git clone git@github.com:afawcett/declarative-lookup-rollup-summaries.git
git clone git@github.com:financialforcedev/df12-apex-enterprise-patterns.git
git clone git@github.com:financialforcedev/df12-deployment-tools.git
git clone git@github.com:dreamhouseapp/dreamhouse-sfdx.git
git clone git@github.com:financialforcedev/fflib-apex-common.git
git clone git@github.com:financialforcedev/fflib-apex-mocks.git
git clone git@github.com:SalesforceFoundation/HEDAP.git
git clone git@github.com:SalesforceLabs/Milestones-PM.git
git clone git@github.com:abhinavguptas/Salesforce-Lookup-Rollup-Summaries.git
git clone git@github.com:dhoechst/Salesforce-Test-Factory.git
git clone git@github.com:kevinohara80/sfdc-trigger-framework.git
git clone git@github.com:forcedotcom/sfdx-dreamhouse.git
git clone git@github.com:forcedotcom/sfdx-simple.git
git clone git@github.com:mbotos/SmartFactory-for-Force.com.git
git clone git@github.com:twilio/twilio-salesforce.git
git clone git@github.com:metadaddy/Visualforce-Multiselect-Picklist.git
git clone git@github.com:rsoesemann/visualforce-table-grid.git
git clone git@github.com:SalesforceFoundation/visualforce-typeahead.git
```

## Source code cleanup
Only keep `cls` and `trigger` files, starting from every project folder
```bash
cd projects
find . -type f -not -name "*.cls" -and -not -name "*.trigger" -delete
find . -type d -name ".git" -exec rm -r "{}" \;
find . -type d -empty -delete
```

## Remove invalid files
Removing files with invalid apex code, like a template with a placeholder `%%%NAMESPACE%%%` that does not compile.
```bash
cd projects
rm Cumulus/scripts/configure_npsp_default_settings.cls
```
