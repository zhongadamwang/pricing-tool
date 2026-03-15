# Test Case PC-001: Basic Cost-Plus Calculation

## Test Information
**Test ID**: PC-001  
**Test Name**: Basic Cost-Plus Calculation  
**Category**: Price Calculation (PC)  
**Priority**: High  
**Created Date**: March 15, 2026  
**Created By**: TBD  
**Last Updated**: March 15, 2026  

## Test Objective
Verify that the pricing system accurately calculates prices using the cost-plus pricing model with standard markup percentages across different product categories.

## Scope
- Basic cost-plus calculation functionality
- Markup percentage application
- Price rounding rules
- Multiple product categories
- Currency handling

## Preconditions
1. Pricing system is operational and accessible
2. Test data set is loaded with product cost information
3. Cost-plus pricing model is configured with standard parameters
4. Test user has pricing calculation permissions
5. Test environment is isolated from production data

## Test Data
### Products
- Product A: Material cost $100.00, Labor cost $50.00, Overhead $25.00 (Total: $175.00)
- Product B: Material cost $250.00, Labor cost $75.00, Overhead $50.00 (Total: $375.00)
- Product C: Material cost $500.00, Labor cost $200.00, Overhead $100.00 (Total: $800.00)

### Markup Percentages
- Standard markup: 20%
- Premium markup: 35%
- Economy markup: 15%

## Test Steps

### Step 1: Configure Cost-Plus Model
1. Access pricing model configuration interface
2. Select "Cost-Plus" pricing model type
3. Configure markup percentage: 20%
4. Set rounding rules: Round to nearest $0.01
5. Save configuration

**Expected Result**: Model configuration saved successfully

### Step 2: Calculate Price for Product A
1. Select Product A for price calculation
2. Verify cost data displayed: Total cost = $175.00
3. Apply cost-plus model with 20% markup
4. Execute price calculation
5. Review calculated price

**Expected Result**: Calculated price = $210.00 ($175.00 × 1.20)

### Step 3: Calculate Price for Product B  
1. Select Product B for price calculation
2. Verify cost data displayed: Total cost = $375.00
3. Apply cost-plus model with 20% markup
4. Execute price calculation
5. Review calculated price

**Expected Result**: Calculated price = $450.00 ($375.00 × 1.20)

### Step 4: Calculate Price for Product C
1. Select Product C for price calculation
2. Verify cost data displayed: Total cost = $800.00
3. Apply cost-plus model with 20% markup
4. Execute price calculation
5. Review calculated price

**Expected Result**: Calculated price = $960.00 ($800.00 × 1.20)

### Step 5: Test Different Markup Percentages
1. Reconfigure model with 35% premium markup
2. Calculate price for Product A
3. Verify calculated price = $236.25 ($175.00 × 1.35)
4. Reconfigure model with 15% economy markup
5. Calculate price for Product A
6. Verify calculated price = $201.25 ($175.00 × 1.15)

**Expected Result**: Prices calculated correctly for different markup percentages

### Step 6: Validate Calculation Audit Trail
1. Review calculation history for all test products
2. Verify calculation parameters are recorded
3. Check timestamp and user information
4. Validate input and output values

**Expected Result**: Complete audit trail maintained for all calculations

## Pass/Fail Criteria

### Pass Criteria
- All price calculations produce correct mathematical results
- Markup percentages applied accurately
- Rounding rules followed consistently
- Audit trail captures all calculation details
- System performance is acceptable (calculations complete within 5 seconds)

### Fail Criteria
- Any calculation produces incorrect price
- Markup percentages not applied properly
- Rounding errors or inconsistencies
- Missing or incomplete audit information
- System errors or timeouts during calculation

## Actual Results
**Execution Date**: TBD  
**Executed By**: TBD  
**Test Status**: Not Started

| Step | Expected Result | Actual Result | Status | Notes |
|------|----------------|---------------|--------|-------|
| 1 | Model configuration saved | | | |
| 2 | Price = $210.00 | | | |
| 3 | Price = $450.00 | | | |
| 4 | Price = $960.00 | | | |
| 5 | Markup variations work | | | |
| 6 | Audit trail complete | | | |

**Overall Result**: TBD  
**Issues Found**: TBD  
**Recommendations**: TBD

## Dependencies
- Test data must be accurate and complete
- Pricing model configuration interface must be functional
- Cost data integration must be working
- User permissions must be properly configured

## Risks
- Incomplete or inaccurate test data could affect test validity
- System performance issues could prevent completion
- Configuration changes could impact other test cases

## Related Test Cases
- PC-002: Value-Based Price Calculation
- PC-004: Tiered Pricing Calculation
- AW-001: Standard Approval Workflow
- EH-001: Invalid Input Handling

## Notes
- This test focuses only on basic cost-plus calculation
- Advanced features like customer-specific markups are tested separately
- Performance baseline to be established during test execution
- Consider automation for regression testing

---
*Test case created: March 15, 2026*  
*Next review: During test execution phase*