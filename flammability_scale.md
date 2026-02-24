# סקאלת תחומי נפיצות

להלן תרשים הממחיש את סקאלת הנפיצות מ-0 ועד 100% נפח, כולל נקודות LEL, UEL ואזורי התראה.

```mermaid
%%{init: {'theme': 'base', 'themeVariables': { 'primaryColor': '#ff0000', 'edgeLabelBackground':'#ffffff', 'tertiaryColor': '#f4f4f4'}}}%%
graph TD
    subgraph "סקאלת ריכוז מלאה (0% עד 100% נפח)"
        
        %% הגדרת האזורים הוויזואליים
        A[0% - אוויר נקי] --> B(תחום ה- PPM <br/> רעילות וחשיפה)
        B -- "מעבר לסקאלת אחוזים" --> C(תערובת ענייה מדי <br/> Too Lean)
        C --> D{נקודת 100% LEL <br/> תחילת נפיצות}
        D --> E[תחום נפיץ <br/> Explosive Range]
        E --> F{נקודת UEL <br/> סוף נפיצות}
        F --> G(תערובת עשירה מדי <br/> Too Rich)
        G --> H[100% נפח גז <br/> (ללא חמצן)]

        %% הוספת סמני אזהרה
        B -.-> |"נקודת התראה (לרוב 10% LEL)"| C1((אזהרת <br/> 10% LEL))
        
        %% עיצוב צבעוני של הצמתים (Nodes)
        style A fill:#e6ffe6,stroke:#33cc33,stroke-width:2px
        style B fill:#ccffcc,stroke:#33cc33,stroke-width:2px
        style C fill:#ffffcc,stroke:#ffcc00,stroke-width:2px
        style C1 fill:#ffeb3b,stroke:#ffc107,stroke-width:3px,color:black,font-weight:bold
        style D fill:#ff9933,stroke:#ff6600,stroke-width:4px,color:white,font-weight:bold
        style E fill:#ff3333,stroke:#cc0000,stroke-width:4px,color:white,font-weight:bold
        style F fill:#ff9933,stroke:#ff6600,stroke-width:4px,color:white,font-weight:bold
        style G fill:#d9d9d9,stroke:#808080,stroke-width:2px
        style H fill:#a6a6a6,stroke:#404040,stroke-width:2px
    end
