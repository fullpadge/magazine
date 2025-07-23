# Exemples de Configurations et Schedules N8N 📅

## 🕐 Templates de Schedules par Scénario

### Scénario 1: Magazine Quotidien Intensif

**Objectif**: 3-4 articles par jour, couverture maximale

```javascript
// Configuration JSON pour N8N
{
  "schedules": {
    "morning_tech": {
      "cron": "0 7 * * 1-5",
      "personality": "alex_tech",
      "description": "Tech news du matin en semaine"
    },
    "lunch_society": {
      "cron": "0 12 * * 1-5", 
      "personality": "marie_society",
      "description": "Actualités société midi"
    },
    "afternoon_science": {
      "cron": "0 15 * * 1-5",
      "personality": "thomas_science", 
      "description": "Science après-midi"
    },
    "evening_culture": {
      "cron": "0 18 * * 1-5",
      "personality": "lucas_culture",
      "description": "Culture en soirée"
    },
    "weekend_economy": {
      "cron": "0 10 * * 6,0",
      "personality": "sophie_economy",
      "description": "Économie weekend"
    }
  }
}
```

### Scénario 2: Magazine Hebdomadaire Premium

**Objectif**: 1-2 articles par jour, qualité maximale

```javascript
{
  "schedules": {
    "monday_tech_analysis": {
      "cron": "0 9 * * 1",
      "personality": "alex_tech",
      "search_depth": "deep",
      "article_length": "long",
      "description": "Analyse tech hebdomadaire"
    },
    "tuesday_society_investigation": {
      "cron": "0 14 * * 2",
      "personality": "marie_society",
      "search_depth": "investigative", 
      "article_length": "very_long",
      "description": "Enquête société approfondie"
    },
    "wednesday_science_breakthrough": {
      "cron": "0 10 * * 3",
      "personality": "thomas_science",
      "search_depth": "academic",
      "article_length": "medium",
      "description": "Découvertes scientifiques"
    },
    "thursday_economy_trends": {
      "cron": "0 16 * * 4",
      "personality": "sophie_economy", 
      "search_depth": "market_analysis",
      "article_length": "long",
      "description": "Tendances économiques"
    },
    "friday_culture_review": {
      "cron": "0 19 * * 5",
      "personality": "lucas_culture",
      "search_depth": "creative",
      "article_length": "medium", 
      "description": "Critiques culturelles weekend"
    }
  }
}
```

### Scénario 3: Magazine Spécialisé Tech

**Objectif**: Focus tech exclusif, multiple angles

```javascript
{
  "schedules": {
    "startup_monday": {
      "cron": "0 8 * * 1",
      "personality": "alex_tech",
      "keywords": "startup+financement+levée+fonds",
      "description": "Actualités startup"
    },
    "ai_tuesday": {
      "cron": "0 8 * * 2", 
      "personality": "alex_tech",
      "keywords": "intelligence+artificielle+machine+learning+LLM",
      "description": "Focus IA"
    },
    "cybersecurity_wednesday": {
      "cron": "0 8 * * 3",
      "personality": "alex_tech",
      "keywords": "cybersécurité+hacking+protection+données",
      "description": "Sécurité informatique"
    },
    "hardware_thursday": {
      "cron": "0 8 * * 4",
      "personality": "alex_tech", 
      "keywords": "hardware+processeur+GPU+smartphone+gadget",
      "description": "Matériel et gadgets"
    },
    "crypto_friday": {
      "cron": "0 8 * * 5",
      "personality": "alex_tech",
      "keywords": "crypto+blockchain+bitcoin+ethereum+DeFi",
      "description": "Cryptomonnaies et blockchain"
    }
  }
}
```

---

## 🎭 Configurations Avancées des Personnalités

### Alex Tech - Configuration Complète

```json
{
  "personality_id": "alex_tech",
  "profile": {
    "name": "Alex Dubois",
    "title": "Journaliste Tech Senior",
    "bio": "Expert en technologies émergentes avec 10 ans d'expérience dans la couverture des innovations tech.",
    "avatar_style": "professional, tech-savvy, modern",
    "expertise": [
      "Intelligence Artificielle",
      "Startups & Fintech", 
      "Cybersécurité",
      "Hardware & Gadgets",
      "Blockchain & Crypto"
    ]
  },
  "writing_config": {
    "style": "analytique_accessible",
    "tone": "professionnel_enthousiaste", 
    "length": {
      "min_words": 800,
      "max_words": 1200,
      "target_words": 1000
    },
    "structure": [
      "hook_introduction",
      "technical_analysis", 
      "market_impact",
      "future_implications",
      "conclusion_actionable"
    ],
    "vocabulary": {
      "level": "expert_vulgarized",
      "buzzwords": ["disruptif", "scalable", "game-changer", "écosystème"],
      "avoid": ["jargon_technique_non_expliqué", "hype_excessif"]
    }
  },
  "search_config": {
    "primary_keywords": [
      "intelligence artificielle",
      "startup technologie", 
      "innovation numérique",
      "cybersécurité entreprise",
      "blockchain applications"
    ],
    "sources_priority": [
      "techcrunch.com",
      "wired.com", 
      "arstechnica.com",
      "venturebeat.com",
      "theverge.com"
    ],
    "time_filter": "24h",
    "geo_filter": "international_francophone"
  },
  "content_prompts": {
    "article_generation": "En tant qu'Alex, journaliste tech expert, analysez cette actualité technologique avec votre expertise unique. Structurez votre article selon votre méthode éprouvée : introduction accrocheuse qui contextualise l'innovation, analyse technique détaillée mais accessible, évaluation de l'impact sur le marché et les utilisateurs, et perspectives d'évolution. Votre ton doit rester professionnel mais passionné, en évitant le sensationnalisme tout en rendant le sujet captivant.",
    "image_generation": "Créez une image représentant l'innovation technologique décrite dans l'article d'Alex. Style moderne et professionnel, évoquant l'avenir et l'innovation. Couleurs tech (bleus, argentés), composition épurée et impactante.",
    "social_media": "Alex partage son analyse tech avec sa communauté. Ton expert mais accessible, focus sur l'insight clé de l'article."
  }
}
```

### Marie Société - Configuration Complète

```json
{
  "personality_id": "marie_society",
  "profile": {
    "name": "Marie Laurent",
    "title": "Journaliste d'Investigation",
    "bio": "Spécialiste des enjeux sociétaux, diplômée en sciences politiques, 8 ans d'expérience en investigation.",
    "avatar_style": "professional, determined, approachable",
    "expertise": [
      "Justice Sociale",
      "Politiques Publiques",
      "Éducation & Santé",
      "Environnement",
      "Droits Humains"
    ]
  },
  "writing_config": {
    "style": "investigatif_nuance",
    "tone": "serieux_objectif_engage",
    "length": {
      "min_words": 1000,
      "max_words": 1500, 
      "target_words": 1250
    },
    "structure": [
      "contexte_historique",
      "presentation_enjeux",
      "enquete_methodique",
      "temoignages_sources",
      "analyse_critique",
      "conclusions_nuancees"
    ],
    "methodology": {
      "fact_checking": "obligatoire",
      "multiple_sources": "minimum_3",
      "neutrality": "perspectives_multiples"
    }
  },
  "search_config": {
    "primary_keywords": [
      "justice sociale France",
      "politique publique impact",
      "inégalités société",
      "mouvement citoyen",
      "réforme sociale"
    ],
    "sources_priority": [
      "lemonde.fr",
      "liberation.fr",
      "mediapart.fr", 
      "franceinfo.fr",
      "reuters.com"
    ],
    "investigation_tools": [
      "fact_checking_apis",
      "government_databases",
      "ngo_reports"
    ]
  },
  "content_prompts": {
    "article_generation": "En tant que Marie, journaliste d'investigation rigoureuse, traitez ce sujet sociétal avec votre méthodologie éprouvée. Commencez par contextualiser historiquement et socialement, présentez les enjeux de manière équilibrée, menez votre enquête en recoupant les sources, donnez la parole aux différents acteurs concernés, et proposez une analyse critique nuancée. Votre objectif : éclairer sans parti pris, informer sans simplifier.",
    "image_generation": "Image représentant l'enjeu sociétal traité par Marie. Style documentaire et humain, mettant en avant les personnes concernées. Composition réaliste et respectueuse.",
    "social_media": "Marie partage son enquête pour sensibiliser aux enjeux sociétaux. Ton engagé mais factuel."
  }
}
```

---

## ⚙️ Configurations Techniques Spécialisées

### Configuration Recherche Avancée

```json
{
  "search_strategies": {
    "breaking_news": {
      "time_filter": "1h",
      "sources": ["reuters", "afp", "ap_news"],
      "keywords_boost": "urgence+breaking+dernière+heure",
      "processing_priority": "immediate"
    },
    "deep_investigation": {
      "time_filter": "7d", 
      "sources": ["academic", "government", "ngo"],
      "research_depth": "multi_layer",
      "fact_check": "mandatory"
    },
    "trend_analysis": {
      "time_filter": "30d",
      "social_signals": "twitter_trends+google_trends",
      "pattern_detection": "enabled",
      "future_prediction": "basic"
    }
  }
}
```

### Configuration Qualité & SEO

```json
{
  "quality_control": {
    "content_checks": {
      "plagiarism": {
        "threshold": 15,
        "api": "copyscape"
      },
      "readability": {
        "flesch_score": ">60",
        "avg_sentence_length": "<25_words"
      },
      "seo_optimization": {
        "keyword_density": "1-3%",
        "meta_description": "auto_generate",
        "title_optimization": "enabled"
      }
    },
    "validation_rules": {
      "min_sources": 3,
      "fact_check_score": ">80%",
      "originality_score": ">90%"
    }
  }
}
```

### Configuration Multi-Langue

```json
{
  "localization": {
    "primary_language": "fr",
    "secondary_languages": ["en", "es"],
    "translation_strategy": {
      "method": "ai_assisted",
      "cultural_adaptation": true,
      "local_sources": true
    },
    "publication_schedule": {
      "fr": "primary_schedule",
      "en": "+2h_offset", 
      "es": "+4h_offset"
    }
  }
}
```

---

## 🔄 Workflows Spécialisés

### Workflow Breaking News

```json
{
  "name": "Breaking_News_Handler",
  "trigger": {
    "type": "webhook",
    "source": "news_alert_apis"
  },
  "processing": {
    "urgency_detection": true,
    "fast_track_writing": true,
    "minimal_fact_check": true,
    "immediate_publication": true
  },
  "execution_time": "<5_minutes",
  "notification": "immediate_all_channels"
}
```

### Workflow Week-end Curation

```json
{
  "name": "Weekend_Curation",
  "trigger": {
    "type": "schedule", 
    "cron": "0 10 * * 6"
  },
  "processing": {
    "week_analysis": true,
    "best_articles_selection": true,
    "trend_identification": true,
    "newsletter_generation": true
  },
  "content_type": "compilation",
  "length": "extended"
}
```

### Workflow Saison/Événements

```json
{
  "name": "Seasonal_Content",
  "triggers": [
    {
      "type": "calendar_event",
      "events": ["CES", "MWC", "Elections", "Nobel_Prize"]
    }
  ],
  "processing": {
    "event_context": true,
    "historical_comparison": true,
    "expert_predictions": true,
    "special_formatting": true
  },
  "personalities": "event_specific_selection"
}
```

---

## 📊 Templates de Monitoring

### Dashboard KPIs Principal

```json
{
  "kpis_dashboard": {
    "production_metrics": {
      "articles_published_today": "count",
      "success_rate_24h": "percentage",
      "avg_execution_time": "minutes", 
      "api_costs_daily": "euros"
    },
    "quality_metrics": {
      "avg_readability_score": "flesch_index",
      "plagiarism_flags": "count",
      "fact_check_accuracy": "percentage",
      "seo_score_avg": "1-100"
    },
    "engagement_metrics": {
      "avg_views_per_article": "number",
      "social_shares_total": "count",
      "comment_engagement": "ratio",
      "bounce_rate": "percentage"
    }
  }
}
```

### Alertes Automatiques

```json
{
  "alert_system": {
    "critical_alerts": {
      "workflow_failure": {
        "threshold": "any_failure",
        "notification": ["slack", "email", "sms"],
        "escalation": "immediate"
      },
      "api_quota_exceeded": {
        "threshold": "90%",
        "notification": ["slack", "email"],
        "action": "pause_workflows"
      }
    },
    "warning_alerts": {
      "quality_degradation": {
        "threshold": "score_<70",
        "notification": ["slack"],
        "action": "flag_for_review"
      },
      "cost_spike": {
        "threshold": "+50%_daily_avg",
        "notification": ["email"],
        "action": "cost_analysis_report"
      }
    }
  }
}
```

---

## 🚀 Templates d'Évolution

### Phase Expansion - Nouvelles Personnalités

```json
{
  "new_personalities": {
    "emma_health": {
      "specialty": "Santé & Médecine",
      "launch_date": "month_2",
      "schedule": "0 11 * * 2,4"
    },
    "jules_sport": {
      "specialty": "Sport & Performance", 
      "launch_date": "month_3",
      "schedule": "0 17 * * 1,3,5"
    },
    "clara_travel": {
      "specialty": "Voyage & Lifestyle",
      "launch_date": "month_4", 
      "schedule": "0 14 * * 6,0"
    }
  }
}
```

### Phase Intelligence - IA Avancée

```json
{
  "ai_enhancement": {
    "trend_prediction": {
      "implementation": "month_6",
      "technology": "time_series_analysis",
      "accuracy_target": ">75%"
    },
    "auto_optimization": {
      "schedule_optimization": "based_on_engagement",
      "personality_matching": "topic_ai_selection", 
      "content_personalization": "reader_behavior_analysis"
    },
    "interaction_ai": {
      "comment_responses": "personality_consistent",
      "social_media_engagement": "automated",
      "reader_questions": "ai_powered_answers"
    }
  }
}
```

---

*Ces configurations vous permettent d'adapter le système à vos besoins spécifiques et d'évoluer progressivement vers un magazine automatisé de plus en plus sophistiqué.*