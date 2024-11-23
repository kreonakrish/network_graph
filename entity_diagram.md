graph TD
  %% Define nodes (entities)
  A[Application] -->|Supports| B[Business Product]
  B -->|Owned By| BO[Business Owner]
  BO -->|Part Of| BH[Business Hierarchy]
  B -->|Funded By| C[Cost Center]
  C -->|Allocates| D[Allocated Budget]
  A -->|Uses| DS[Data Set]
  A -->|Managed By| TO[Tech Owner]
  TO -->|Part Of| TH[Tech Management Hierarchy]
  TO -->|Belongs To| TDH[Tech Department Hierarchy]

  %% Add sample nodes for clarity
  subgraph Applications
    CRM["CRM System"]
    RMS["Risk Management System"]
  end
  subgraph Business Products
    Retail["Retail Banking"]
    Commercial["Commercial Banking"]
  end
  subgraph Cost Centers
    ITBudget["IT Budget"]
    RetailBudget["Retail Budget"]
  end

  %% Sample Relationships
  CRM -->|Supports| Retail
  RMS -->|Supports| Commercial
  Retail -->|Funded By| RetailBudget
  Commercial -->|Funded By| ITBudget
  CRM -->|Managed By| JohnDoe[John Doe]
  JohnDoe -->|Part Of| ITOps[IT Operations]
  CRM -->|Uses| CustomerRecords["Customer Records"]
  RMS -->|Uses| FraudPatterns["Fraud Patterns"]
