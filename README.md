import { Card } from "@/components/ui/card";
import { Brain, TrendingUp, Shield, BarChart3, Zap, Users, LineChart } from "lucide-react";

const services = [
  {
    icon: Brain,
    title: "Análisis Financiero Automatizado",
    items: [
      "Diagnóstico financiero integral usando algoritmos de IA",
      "Revisión de estados financieros con detección de anomalías",
      "Indicadores KPI automatizados"
    ]
  },
  {
    icon: TrendingUp,
    title: "Modelos de Predicción Financiera",
    items: [
      "Proyección de ventas y flujo de caja",
      "Predicción de gastos y costos operativos",
      "Modelos predictivos de demanda y rentabilidad"
    ]
  },
  {
    icon: BarChart3,
    title: "Optimización de Presupuestos",
    items: [
      "Creación de presupuestos inteligentes basados en datos históricos",
      "Alertas de desviaciones presupuestarias en tiempo real",
      "Recomendaciones automáticas para reducción de costos"
    ]
  },
  {
    icon: Shield,
    title: "Gestión de Riesgos con IA",
    items: [
      "Detección temprana de riesgos de liquidez",
      "Análisis de riesgo de clientes (credit scoring)",
      "Evaluación del impacto de escenarios económicos"
    ]
  },
  {
    icon: Zap,
    title: "Automatización Financiera",
    items: [
      "Automatización de conciliaciones",
      "Clasificación inteligente de transacciones",
      "Integración con sistemas contables (ERP/CRM)"
    ]
  },
  {
    icon: Users,
    title: "Asesoría Estratégica con IA",
    items: [
      "Simulación y análisis de escenarios (\"what-if\")",
      "Optimización del portafolio de inversiones",
      "Estrategias de crecimiento basadas en datos"
    ]
  },
  {
    icon: LineChart,
    title: "Dashboards Financieros Inteligentes",
    items: [
      "Paneles en tiempo real con visualizaciones dinámicas",
      "Alertas automatizadas por email/WhatsApp",
      "Informes financieros generados por IA"
    ]
  },
];

const Services = () => {
  return (
    <section className="py-24 bg-muted">
      <div className="container mx-auto px-6">
        <div className="text-center mb-16">
          <h2 className="text-4xl md:text-5xl font-bold text-foreground mb-4">
            Servicios Financieros con IA
          </h2>
          <p className="text-xl text-muted-foreground max-w-2xl mx-auto">
            Aprovecha la inteligencia artificial para transformar tu estrategia financiera y lograr resultados sin precedentes.
          </p>
        </div>

        <div className="grid md:grid-cols-2 lg:grid-cols-3 gap-8">
          {services.map((service, index) => (
            <Card 
              key={index}
              className="p-8 hover:shadow-strong transition-all duration-300 hover:-translate-y-1 bg-card border-border group"
            >
              <div className="w-14 h-14 bg-gradient-accent rounded-xl flex items-center justify-center mb-6 group-hover:scale-110 transition-transform">
                <service.icon className="w-7 h-7 text-accent-foreground" />
              </div>
              <h3 className="text-2xl font-semibold text-card-foreground mb-4">
                {service.title}
              </h3>
              <ul className="space-y-3">
                {service.items.map((item, itemIndex) => (
                  <li key={itemIndex} className="flex items-start gap-2 text-muted-foreground">
                    <span className="text-primary mt-1 flex-shrink-0">•</span>
                    <span className="leading-relaxed">{item}</span>
                  </li>
                ))}
              </ul>
            </Card>
          ))}
        </div>
      </div>
    </section>
  );
};

export default Services;
