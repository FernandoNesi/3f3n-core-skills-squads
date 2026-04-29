{
  "version": "2.0",
  "skills": [
	{
	  "id": "conversion-structure-3f3n",
	  "name": "Conversion Structure",
	  "type": "conversion",
	  "level": "engine",
	  "priority": "high",
	
	  "role": "structure",
	  "stage": "creation",
	
	  "description": "Cria estrutura completa de página de alta conversão baseada nas 14 lâminas",
	
	  "input": {
		"required": ["ideia"],
		"optional": ["publico", "ticket", "contexto"]
	  },
	
	  "output": {
		"format": "markdown",
		"sections": [
		  "headline",
		  "subheadline",
		  "promessa",
		  "mecanismo",
		  "prova",
		  "beneficios",
		  "objecoes",
		  "oferta",
		  "cta"
		]
	  },
	
	  "execution": {
		"mode": "sequential",
		"autonomy": "assisted"
	  },
	
	  "rules": {
		"must": [
		  "seguir logica de conversao",
		  "manter clareza",
		  "focar em decisao"
		],
		"must_not": [
		  "criar estrutura confusa",
		  "ser genérico"
		]
	  },
	
	  "dependencies": [],
	
	  "compatible_with": [
		"conversion-headline-3f3n",
		"conversion-offer-3f3n",
		"conversion-proof-3f3n",
		"conversion-cta-3f3n"
	  ],
	
	  "tags": ["structure", "landing", "conversion"],
	
	  "example_use": "/3f3n-create-landing"
	},

    {
      "id": "conversion-audit-3f3n",
      "name": "Conversion Audit",
      "type": "conversion",
      "level": "engine",
      "priority": "high",
      "role": "diagnosis",
      "stage": "analysis",
      "description": "Identifica onde a página perde conversão e por quê",
      "input": {
        "required": ["pagina"],
        "optional": ["contexto", "objetivo"]
      },
      "output": {
        "format": "markdown",
        "sections": ["diagnostico", "impacto", "falhas"]
      },
      "execution": {
        "mode": "sequential",
        "autonomy": "assisted"
      },
      "rules": {
        "must": [
          "focar em conversao",
          "priorizar impacto financeiro",
          "ser direto"
        ],
        "must_not": [
          "avaliar design",
          "ser genérico"
        ]
      },
      "dependencies": [],
      "compatible_with": [
        "conversion-performance-3f3n",
        "conversion-optimizer-3f3n"
      ],
      "tags": ["conversion", "analysis"],
      "example_use": "/3f3n-optimize-landing"
    },

    {
      "id": "conversion-performance-3f3n",
      "name": "Conversion Performance",
      "type": "conversion",
      "level": "engine",
      "priority": "high",
      "role": "performance",
      "stage": "analysis",
      "description": "Identifica problemas de carregamento que impactam conversão",
      "input": {
        "required": ["pagina"],
        "optional": ["contexto"]
      },
      "output": {
        "format": "markdown",
        "sections": ["problemas", "impacto", "prioridades"]
      },
      "execution": {
        "mode": "sequential",
        "autonomy": "assisted"
      },
      "rules": {
        "must": [
          "focar em impacto na conversao",
          "priorizar mobile",
          "ser prático"
        ],
        "must_not": [
          "focar apenas em técnica",
          "ser genérico"
        ]
      },
      "dependencies": [],
      "compatible_with": [
        "conversion-audit-3f3n",
        "conversion-optimizer-3f3n"
      ],
      "tags": ["performance", "conversion"]
    },

    {
      "id": "conversion-optimizer-3f3n",
      "name": "Conversion Optimizer",
      "type": "conversion",
      "level": "engine",
      "priority": "high",
      "role": "execution",
      "stage": "optimization",
      "description": "Corrige erros críticos de conversão com base no diagnóstico",
      "input": {
        "required": ["diagnostico"],
        "optional": ["contexto"]
      },
      "output": {
        "format": "markdown",
        "sections": ["correcoes", "copy", "plano"]
      },
      "execution": {
        "mode": "sequential",
        "autonomy": "assisted"
      },
      "rules": {
        "must": [
          "resolver alto impacto",
          "gerar copy pronta",
          "ser direto"
        ],
        "must_not": [
          "explicar demais",
          "ser genérico"
        ]
      },
      "dependencies": ["conversion-audit-3f3n"],
      "compatible_with": [
        "conversion-headline-3f3n",
        "conversion-cta-3f3n",
        "conversion-proof-3f3n"
      ],
      "tags": ["conversion", "execution"]
    },

    {
      "id": "conversion-headline-3f3n",
      "name": "Conversion Headline",
      "type": "component",
      "level": "component",
      "priority": "high",
      "role": "headline",
      "stage": "optimization",
      "description": "Cria headlines de alta conversão",
      "input": {
        "required": ["contexto"],
        "optional": ["oferta"]
      },
      "output": {
        "format": "list",
        "items": 10
      },
      "execution": {
        "mode": "single",
        "autonomy": "assisted"
      },
      "rules": {
        "must": [
          "ser clara",
          "ser direta",
          "gerar impacto imediato"
        ],
        "must_not": [
          "ser vaga",
          "ser longa"
        ]
      },
      "dependencies": [],
      "tags": ["headline", "copy"]
    },

    {
      "id": "conversion-cta-3f3n",
      "name": "Conversion CTA",
      "type": "component",
      "level": "component",
      "priority": "high",
      "role": "cta",
      "stage": "optimization",
      "description": "Cria CTAs de alta conversão",
      "input": {
        "required": ["contexto"]
      },
      "output": {
        "format": "list",
        "items": 10
      },
      "execution": {
        "mode": "single"
      },
      "rules": {
        "must": [
          "ser acionável",
          "ser clara"
        ],
        "must_not": [
          "ser genérica"
        ]
      },
      "dependencies": [],
      "tags": ["cta", "conversion"]
    },

    {
      "id": "conversion-offer-3f3n",
      "name": "Conversion Offer",
      "type": "component",
      "level": "component",
      "priority": "high",
      "role": "offer",
      "stage": "structure",
      "description": "Cria ofertas de alto valor percebido",
      "input": {
        "required": ["produto", "preco"]
      },
      "output": {
        "format": "markdown",
        "sections": ["oferta", "bonus", "garantia"]
      },
      "rules": {
        "must": [
          "aumentar valor percebido"
        ],
        "must_not": [
          "ser confusa"
        ]
      },
      "dependencies": [],
      "tags": ["offer"]
    },

    {
      "id": "conversion-proof-3f3n",
      "name": "Conversion Proof",
      "type": "component",
      "level": "component",
      "priority": "high",
      "role": "proof",
      "stage": "trust",
      "description": "Cria provas que aumentam confiança",
      "input": {
        "required": ["contexto"]
      },
      "output": {
        "format": "markdown",
        "sections": ["prova_social", "prova_logica"]
      },
      "rules": {
        "must": [
          "ser concreta"
        ],
        "must_not": [
          "ser vaga"
        ]
      },
      "dependencies": [],
      "tags": ["proof"]
    },

    {
      "id": "conversion-reviewer-3f3n",
      "name": "Conversion Reviewer",
      "type": "system",
      "level": "system",
      "priority": "high",
      "role": "refinement",
      "stage": "review",
      "description": "Refina outputs para melhorar clareza e impacto",
      "input": {
        "required": ["conteudo"]
      },
      "output": {
        "format": "markdown"
      },
      "rules": {
        "must": [
          "simplificar",
          "melhorar clareza"
        ],
        "must_not": [
          "aumentar complexidade"
        ]
      },
      "dependencies": [],
      "tags": ["review"]
    },

    {
      "id": "conversion-score-3f3n",
      "name": "Conversion Score",
      "type": "analysis",
      "level": "system",
      "priority": "medium",
      "role": "validation",
      "stage": "review",
      "description": "Avalia qualidade de conversão",
      "input": {
        "required": ["conteudo"]
      },
      "output": {
        "format": "markdown",
        "sections": ["score", "falhas"]
      },
      "rules": {
        "must": [
          "ser objetivo"
        ],
        "must_not": [
          "ser subjetivo"
        ]
      },
      "dependencies": [],
      "tags": ["score"]
    },

    {
      "id": "project-init-3f3n-nextjs",
      "name": "Project Init 3F3N",
      "type": "system",
      "level": "system",
      "priority": "high",
      "role": "bootstrap",
      "stage": "setup",
      "description": "Cria projeto Next.js com padrão 3F3N e integra core",
      "input": {
        "required": ["nome"],
        "optional": ["tipo"]
      },
      "output": {
        "format": "filesystem"
      },
      "execution": {
        "mode": "setup"
      },
      "rules": {
        "must": [
          "criar estrutura modular",
          "incluir 3f3n-core",
          "gerar gitignore"
        ],
        "must_not": [
          "criar estrutura monolítica"
        ]
      },
      "dependencies": [],
      "tags": ["setup", "nextjs"]
    },

    {
	  "id": "conversion-elementor-3f3n",
	  "name": "Conversion Elementor",
	  "type": "conversion",
	  "level": "component",
	  "priority": "high",
	
	  "role": "element-optimizer",
	  "stage": "optimization",
	
	  "description": "Otimiza um elemento específico para maximizar conversão",
	
	  "input": {
	    "required": ["elemento"],
	    "optional": ["contexto", "objetivo"]
	  },
	
	  "output": {
	    "format": "markdown",
	    "sections": [
	      "diagnostico",
	      "correcao",
	      "execucao"
	    ]
	  },
	
	  "execution": {
	    "mode": "single",
	    "autonomy": "assisted"
	  },
	
	  "rules": {
	    "must": [
	      "ser direto e cirúrgico",
	      "focar em decisão de compra",
	      "gerar copy pronta",
	      "priorizar impacto financeiro"
	    ],
	    "must_not": [
	      "ser genérico",
	      "focar em design superficial",
	      "explicar demais"
	    ]
	  },
	
	  "dependencies": [],
	
	  "compatible_with": [
	    "conversion-audit-3f3n",
	    "conversion-optimizer-3f3n",
	    "conversion-reviewer-3f3n"
	  ],
	
	  "tags": [
	    "conversion",
	    "element",
	    "optimization",
	    "copy"
	  ],
	
	  "example_use": "otimizar headline, CTA, seção específica"
	}

  ]
}