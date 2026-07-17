# HR Analytics: Attrition, Training ROI & Pay Equity

## Cíl projektu
Cílem projektu je analyzovat HR data fiktivní/anonymizované firmy a odpovědět na
klíčové otázky, které by v praxi řešilo HR nebo management oddělení: proč
zaměstnanci odcházejí, jestli se firmě vyplácí investice do školení a jestli
existují neopodstatněné rozdíly v odměňování napříč skupinami zaměstnanců.
Projekt demonstruje celý analytický proces – od čištění dat přes SQL a pandas
analýzu až po vizualizace a konkrétní doporučení.

## Otázky, na které odpovídám
1. Jaké faktory nejvíc souvisí s odchodem zaměstnanců (attrition)?
2. Vyplácí se firmě investice do školení – mění se satisfaction/performance po tréninku?
3. Existují neopodstatněné rozdíly v platu nebo povýšení podle genderu/rasy při srovnatelné pozici a zkušenosti?
4. Liší se míra attrition podle konkrétních supervizorů/týmů?

## Data
Zdroj: [HR Analytics Dataset (Kaggle)](https://www.kaggle.com/datasets/hopesb/hr-analytics-dataset)
Dataset obsahuje údaje o zaměstnancích, tréninkových programech, engagement/satisfaction skóre a diverzitních charakteristikách.

**Poznámka k datové governance**: Sloupce s přímou identifikací (jméno, email) byly
z analýzy odstraněny. Sloupec Supervisor byl záměrně ponechán pro analýzu vztahu
mezi vedením týmu a mírou odchodu zaměstnanců.

## Nástroje
- Python (pandas, numpy)
- SQL (SQLite)
- Matplotlib / Seaborn pro vizualizace
- Jupyter Notebook

## Struktura repozitáře
hr-analytics/
├── data/               # surová a vyčištěná data
├── notebooks/          # Jupyter notebooky s analýzou
├── sql/                # SQL dotazy
├── visuals/             # exportované grafy
└── README.md
## Klíčová zjištění
Analyzovali jsme vztah mezi odchodem zaměstnanců (51,1% míra) a dostupnými proměnnými — satisfaction, engagement, work-life balance skóre, performance hodnocení, věkem a business unit. Žádná z těchto proměnných nevykazuje silný vztah k attrition, což naznačuje buď náhodné rozložení v datech, nebo že skutečné důvody odchodu (mzda, kariérní příležitosti, externí nabídky) nejsou v datasetu zachyceny. Sloupec Supervisor navíc neumožňuje týmovou analýzu, protože průměrně spravuje jen 1 podřízeného.

## Jak spustit projekt
