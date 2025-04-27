# uml# Random Data Visualization with Mermaid

## 1. Monthly Sales Data (2024)

| Month      | Sales (in $1000s) |
|------------|-------------------|
| January    | 45                |
| February   | 58                |
| March      | 72                |
| April      | 65                |
| May        | 81                |
| June       | 95                |
| July       | 112               |
| August     | 108               |
| September  | 89                |
| October    | 76                |
| November   | 68                |
| December   | 83                |

### Sales Trend Chart

```mermaid
graph TD
    title[Monthly Sales Trend 2024]
    style title fill:#f9f9f9,stroke:#333,stroke-width:1px

    %% Using a bar chart to represent sales data
    subgraph Monthly Sales
    Jan[Jan: $45k]
    Feb[Feb: $58k]
    Mar[Mar: $72k]
    Apr[Apr: $65k]
    May[May: $81k]
    Jun[Jun: $95k]
    Jul[Jul: $112k]
    Aug[Aug: $108k]
    Sep[Sep: $89k]
    Oct[Oct: $76k]
    Nov[Nov: $68k]
    Dec[Dec: $83k]
    end
```

### Bar Chart Visualization

```mermaid
%%{init: {'theme': 'base', 'themeVariables': { 'primaryColor': '#5D8AA8', 'secondaryColor': '#A0CBE8'}}}%%
xychart-beta
    title "Monthly Sales (2024)"
    x-axis [Jan, Feb, Mar, Apr, May, Jun, Jul, Aug, Sep, Oct, Nov, Dec]
    y-axis "Sales ($1000s)"
    bar [45, 58, 72, 65, 81, 95, 112, 108, 89, 76, 68, 83]
```

## 2. Product Category Distribution

| Category       | Market Share (%) |
|----------------|------------------|
| Electronics    | 32               |
| Clothing       | 28               |
| Home Goods     | 17               |
| Food & Beverage| 14               |
| Other          | 9                |

### Pie Chart Visualization

```mermaid
pie title Product Category Market Share
    "Electronics" : 32
    "Clothing" : 28
    "Home Goods" : 17
    "Food & Beverage" : 14
    "Other" : 9
```

## 3. Customer Acquisition Flow

### Flowchart

```mermaid
flowchart LR
    A[Website Visit] -->|40%| B[Sign Up]
    A -->|60%| C[Bounce]
    B -->|70%| D[Complete Profile]
    B -->|30%| E[Abandon]
    D -->|80%| F[Make Purchase]
    D -->|20%| G[Inactive Account]
    
    style A fill:#f5f5f5,stroke:#333,stroke-width:2px
    style B fill:#d5e8d4,stroke:#82b366,stroke-width:2px
    style C fill:#f8cecc,stroke:#b85450,stroke-width:2px
    style D fill:#d5e8d4,stroke:#82b366,stroke-width:2px
    style E fill:#f8cecc,stroke:#b85450,stroke-width:2px
    style F fill:#dae8fc,stroke:#6c8ebf,stroke-width:2px
    style G fill:#fff2cc,stroke:#d6b656,stroke-width:2px
```

## 4. Project Timeline

### Gantt Chart

```mermaid
gantt
    title Project Timeline 2024
    dateFormat  YYYY-MM-DD
    
    section Research
    Market Analysis      :a1, 2024-01-10, 30d
    User Interviews      :a2, after a1, 25d
    
    section Development
    Design Phase         :b1, 2024-02-15, 45d
    Implementation       :b2, after b1, 60d
    Testing              :b3, after b2, 30d
    
    section Launch
    Marketing Campaign   :c1, 2024-05-01, 45d
    Product Launch       :milestone, after b3, 0d
    Post-Launch Analysis :c2, after c1, 20d
```

## 5. Team Organization

### Organizational Chart

```mermaid
%%{init: {'theme': 'forest'}}%%
flowchart TD
    CEO[CEO: Sarah Johnson] --> CTO[CTO: Michael Chen]
    CEO --> CMO[CMO: David Smith]
    CEO --> CFO[CFO: Lisa Wong]
    
    CTO --> DevMgr[Dev Manager: Alex Kumar]
    CTO --> DataMgr[Data Science Lead: Maria Rodriguez]
    
    DevMgr --> Dev1[Sr. Developer: Jane Doe]
    DevMgr --> Dev2[Sr. Developer: John Smith]
    DevMgr --> Dev3[Jr. Developer: Emma Wilson]
    
    DataMgr --> DS1[Data Scientist: Tom Brown]
    DataMgr --> DS2[Data Analyst: Chris Lee]
    
    CMO --> MarketMgr[Marketing Manager: Patricia Lopez]
    MarketMgr --> Mark1[Content Specialist: Ryan Taylor]
    MarketMgr --> Mark2[Social Media: Zoe Adams]
    
    CFO --> Finance1[Financial Analyst: Kevin Park]
    CFO --> Finance2[Accountant: Jasmine Chen]
    
    classDef executive fill:#f9d5e5,stroke:#333,stroke-width:1px
    classDef manager fill:#eeeeee,stroke:#333,stroke-width:1px
    classDef employee fill:#d5e8d4,stroke:#333,stroke-width:1px
    
    class CEO,CTO,CMO,CFO executive
    class DevMgr,DataMgr,MarketMgr manager
    class Dev1,Dev2,Dev3,DS1,DS2,Mark1,Mark2,Finance1,Finance2 employee
```

## 6. User Registration Stats by Region (Q1 2024)

| Region      | January | February | March | Total |
|-------------|---------|----------|-------|-------|
| North America | 1240  | 1580     | 1890  | 4710  |
| Europe      | 980     | 1250     | 1420  | 3650  |
| Asia        | 1650    | 1830     | 2120  | 5600  |
| Others      | 420     | 510      | 670   | 1600  |

### Line Chart Visualization

```mermaid
%%{init: {'theme': 'neutral'}}%%
xychart-beta
    title "User Registrations by Region (Q1 2024)"
    x-axis [January, February, March]
    y-axis "Number of Users"
    line [1240, 1580, 1890]
    line [980, 1250, 1420]
    line [1650, 1830, 2120]
    line [420, 510, 670]
    legend [North America, Europe, Asia, Others]
```

## 7. User Journey Map

### State Diagram

```mermaid
stateDiagram-v2
    [*] --> Awareness
    Awareness --> Consideration
    Consideration --> Purchase
    Purchase --> Retention
    Retention --> Advocacy
    Retention --> Churn
    Advocacy --> [*]
    Churn --> [*]
    
    state Awareness {
        [*] --> SocialMedia
        [*] --> SearchEngine
        [*] --> Referral
        SocialMedia --> [*]
        SearchEngine --> [*]
        Referral --> [*]
    }
    
    state Consideration {
        [*] --> ProductResearch
        [*] --> ComparisonShopping
        ProductResearch --> [*]
        ComparisonShopping --> [*]
    }
    
    state Purchase {
        [*] --> AddToCart
        AddToCart --> Checkout
        Checkout --> Confirmation
        Confirmation --> [*]
    }
```

## 8. System Architecture

### Component Diagram

```mermaid
%%{init: {'theme': 'default'}}%%
flowchart TB
    subgraph Client
        UI[User Interface]
        State[State Management]
        API_Client[API Client]
    end
    
    subgraph Server
        API[API Layer]
        Auth[Authentication]
        BL[Business Logic]
    end
    
    subgraph Database
        Postgres[PostgreSQL]
        Redis[Redis Cache]
    end
    
    UI <--> State
    State <--> API_Client
    API_Client <--> API
    API <--> Auth
    API <--> BL
    BL <--> Postgres
    BL <--> Redis
    
    classDef client fill:#d0e0ff,stroke:#333,stroke-width:1px
    classDef server fill:#ffffd0,stroke:#333,stroke-width:1px
    classDef database fill:#d0ffcc,stroke:#333,stroke-width:1px
    
    class UI,State,API_Client client
    class API,Auth,BL server
    class Postgres,Redis database
```

## 9. Decision Making Process

### Decision Tree

```mermaid
graph TD
    A[Start: Project Proposal] -->|Evaluate| B{Budget > $50K?}
    B -->|Yes| C{Strategic Priority?}
    B -->|No| D{ROI > 20%?}
    
    C -->|Yes| E[Executive Approval]
    C -->|No| F{ROI > 30%?}
    
    D -->|Yes| G[Department Manager Approval]
    D -->|No| H[Reject Proposal]
    
    F -->|Yes| E
    F -->|No| H
    
    E --> I[Project Kickoff]
    G --> I
    
    style A fill:#f5f5f5,stroke:#333,stroke-width:2px
    style B fill:#d5e8d4,stroke:#82b366,stroke-width:2px
    style C fill:#d5e8d4,stroke:#82b366,stroke-width:2px
    style D fill:#d5e8d4,stroke:#82b366,stroke-width:2px
    style E fill:#dae8fc,stroke:#6c8ebf,stroke-width:2px
    style F fill:#d5e8d4,stroke:#82b366,stroke-width:2px
    style G fill:#dae8fc,stroke:#6c8ebf,stroke-width:2px
    style H fill:#f8cecc,stroke:#b85450,stroke-width:2px
    style I fill:#d5e8d4,stroke:#82b366,stroke-width:2px
```

## 10. Feature Adoption Rate

| Feature     | Week 1 | Week 2 | Week 3 | Week 4 | Week 5 | Week 6 |
|-------------|--------|--------|--------|--------|--------|--------|
| Dashboard   | 10%    | 18%    | 25%    | 35%    | 42%    | 48%    |
| Analytics   | 5%     | 8%     | 15%    | 20%    | 33%    | 45%    |
| Mobile App  | 12%    | 22%    | 35%    | 38%    | 42%    | 46%    |

### Line Chart

```mermaid
xychart-beta
    title "Feature Adoption Rate"
    x-axis [Week 1, Week 2, Week 3, Week 4, Week 5, Week 6]
    y-axis "Adoption Rate (%)"
    line [10, 18, 25, 35, 42, 48]
    line [5, 8, 15, 20, 33, 45]
    line [12, 22, 35, 38, 42, 46]
    legend [Dashboard, Analytics, Mobile App]
```