# Octagon Earnings Transcripts MCP

![Favicon](https://docs.octagonagents.com/logo.svg) The Octagon Earnings Transcripts MCP server provides specialized AI-powered earnings call transcript analysis capabilities by integrating with advanced transcripts analysis agents. Covers over 8,000 public companies with continuous daily updates and historical data dating back to 2018. Add unlimited earnings transcript analysis functionality to any MCP client including Claude Desktop, Cursor, and other popular MCP-enabled applications.

**Powered by [Octagon AI](https://docs.octagonagents.com)** - Learn more about the Transcripts Agent at [docs.octagonagents.com](https://docs.octagonagents.com/guide/agents/transcripts-agent.html)

## 🏆 Why Teams Choose Octagon's Enterprise-Grade Transcripts Analysis API

👉 **8,000+ public companies** with comprehensive earnings call coverage  
👉 **Historical depth** — earnings call data dating back to 2018 for robust time-series analysis  
👉 **Real-time updates** — continuous daily updates for the latest earnings insights  
👉 **Advanced analysis** — extract executive statements, financial guidance, analyst questions, and forward-looking statements  

## 🚀 Core Differentiators

✅ **Comprehensive Coverage** - Over 8,000 public companies with earnings call transcripts  
✅ **Historical Analysis** - Historical data dating back to 2018 enables robust time-series analysis  
✅ **Real-Time Updates** - Continuous daily updates for real-time insights  
✅ **Universal MCP Integration** - Add earnings transcript analysis to any MCP client  
✅ **Multi-Domain Analysis** - Management sentiment, guidance extraction, and business trend identification  
✅ **Advanced Data Extraction** - Executive statements, analyst questions, and forward-looking statements  

## Features

✅ **Comprehensive Transcripts Analysis**
   - Executive statements and commentary extraction
   - Financial guidance and projections analysis
   - Analyst questions and management responses
   - Forward-looking statements identification
   - Management sentiment analysis
   - Key business trends identification
     
✅ **Universal Company Coverage**
   - Over 8,000 public companies
   - Quarterly and annual earnings calls
   - Special earnings announcements
   - Management presentations
   - Investor day transcripts
   - Conference call recordings
     
✅ **Advanced Analysis Tools**
   - Time-series trend analysis
   - Cross-company comparisons
   - Sentiment tracking over time
   - Guidance accuracy analysis


## Get Your Octagon API Key

To use Octagon Earnings Transcripts MCP, you need to:

1. Sign up for a free account at [Octagon](https://app.octagonai.co/signup/?redirectToAfterSignup=https://app.octagonai.co/api-keys)
2. After logging in, from left menu, navigate to **API Keys** 
3. Generate a new API key
4. Use this API key in your configuration as the `OCTAGON_API_KEY` value

## Prerequisites

Before installing or running Octagon Earnings Transcripts MCP, you need to have `npx` (which comes with Node.js and npm) installed on your system.

### Mac (macOS)

1. **Install Homebrew** (if you don't have it):
   ```bash
   /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
   ```
2. **Install Node.js (includes npm and npx):**
   ```bash
   brew install node
   ```
   This will install the latest version of Node.js, npm, and npx.

3. **Verify installation:**
   ```bash
   node -v
   npm -v
   npx -v
   ```

### Windows

1. **Download the Node.js installer:**
   - Go to [https://nodejs.org/](https://nodejs.org/) and download the LTS version for Windows.
2. **Run the installer** and follow the prompts. This will install Node.js, npm, and npx.
3. **Verify installation:**
   Open Command Prompt and run:
   ```cmd
   node -v
   npm -v
   npx -v
   ```

If you see version numbers for all three, you are ready to proceed with the installation steps below.

## Installation

### Running on Claude Desktop

To configure Octagon Earnings Transcripts MCP for Claude Desktop:

1. Open Claude Desktop
2. Go to Settings > Developer > Edit Config
3. Add the following to your `claude_desktop_config.json` (Replace `your-octagon-api-key` with your Octagon API key):
```json
{
  "mcpServers": {
    "octagon-earnings-transcripts-mcp": {
      "command": "npx",
      "args": ["-y", "octagon-earnings-transcripts-mcp@latest"],
      "env": {
        "OCTAGON_API_KEY": "YOUR_API_KEY_HERE"
      }
    }
  }
}
```
4. Restart Claude for the changes to take effect

### Running on Cursor

Configuring Cursor Desktop 🖥️
Note: Requires Cursor version 0.45.6+

To configure Octagon Earnings Transcripts MCP in Cursor:

1. Open Cursor Settings
2. Go to Features > MCP Servers 
3. Click "+ Add New MCP Server"
4. Enter the following:
   - Name: "octagon-earnings-transcripts-mcp" (or your preferred name)
   - Type: "command"
   - Command: `env OCTAGON_API_KEY=your-octagon-api-key npx -y octagon-earnings-transcripts-mcp`

> If you are using Windows and are running into issues, try `cmd /c "set OCTAGON_API_KEY=your-octagon-api-key && npx -y octagon-earnings-transcripts-mcp"`

Replace `your-octagon-api-key` with your Octagon API key.

After adding, refresh the MCP server list to see the new tools. The Composer Agent will automatically use Octagon Earnings Transcripts MCP when appropriate, but you can explicitly request it by describing your earnings analysis needs. Access the Composer via Command+L (Mac), select "Agent" next to the submit button, and enter your query.

### Running on Windsurf

Add this to your `./codeium/windsurf/model_config.json`:

```json
{
  "mcpServers": {
    "octagon-earnings-transcripts-mcp": {
      "command": "npx",
      "args": ["-y", "octagon-earnings-transcripts-mcp@latest"],
      "env": {
        "OCTAGON_API_KEY": "YOUR_API_KEY_HERE"
      }
    }
  }
}
```

### Running with npx

```bash
env OCTAGON_API_KEY=your_octagon_api_key npx -y octagon-earnings-transcripts-mcp
```

### Manual Installation

```bash
npm install -g octagon-earnings-transcripts-mcp
```


# Octagon Transcripts Agent

**Model Name**: `octagon-transcripts-agent`

A specialized agent for analyzing earnings call transcripts and management commentary.

## Capabilities

- Over 8,000 public companies
- Continuous daily updates for real-time insights
- Historical data dating back to 2018 enables robust time-series analysis
- Extract information from earnings call transcripts, including:
  - Executive statements
  - Financial guidance
  - Analyst questions
  - Forward-looking statements

## Use Cases

The Transcripts Agent is best for:
- Analyzing management sentiment
- Extracting guidance figures
- Identifying key business trends
- Tracking narrative changes over time
- Comparing management statements with actual results

## Example Queries

- "What did Amazon's CEO say about AWS growth expectations in the latest earnings call?"
- "Summarize key financial metrics mentioned in Tesla's Q2 2023 earnings call"
- "What questions did analysts ask about margins during Netflix's latest earnings call?"


## How to Create Effective Prompts for Earnings Call Analysis

When analyzing earnings call transcripts, these strategies can help you extract meaningful insights:

1. **Specify the time period**: Indicate whether you're interested in a specific quarter, year, or a comparison across periods.
   - Example: "Extract key revenue figures mentioned in Apple's Q1 2024 earnings call."

2. **Focus on speaker roles**: Request insights from specific participants like the CEO, CFO, or analysts.
   - Example: "Summarize what Amazon's CEO said about AWS growth strategy in their latest earnings call."

3. **Combine quantitative and qualitative data**: Request both numbers and narrative context.
   - Example: "Identify Tesla's projected production targets for 2024 and management's comments on manufacturing challenges."

4. **Target specific business segments**: Focus your query on particular divisions or product lines.
   - Example: "Extract all mentions of Microsoft's cloud services revenue and growth projections from the Q2 earnings call."

5. **Look for sentiment and tone**: Ask for analysis of management confidence or concern.
   - Example: "Analyze the tone used by Netflix executives when discussing subscriber growth in international markets."

6. **Track recurring themes**: Request identification of topics mentioned across multiple calls.
   - Example: "Identify how Meta's messaging about metaverse investments has evolved over the past four earnings calls."

7. **Compare analyst vs. management perspectives**: Contrast questions with answers to uncover tensions.
   - Example: "Compare analyst questions about Google's AI investments with management's responses in the latest earnings call."

8. **Identify forward-looking statements**: Focus on future projections rather than past performance.
   - Example: "Extract all forward-looking statements about Nvidia's supply chain improvements mentioned in the Q3 call."

## Earnings Call Transcript Data Fields

### Call Metadata

| Field | Description |
|-------|-------------|
| Company Name | Legal name of the company holding the earnings call |
| Ticker Symbol | Stock trading symbol of the company |
| Call Date | Date when the earnings call took place |
| Call Time | Time when the earnings call started |
| Call Duration | Length of the earnings call in minutes |
| Fiscal Period | Quarter or year being discussed (e.g., Q1 2024, FY 2023) |
| Call Type | Nature of the call (e.g., Quarterly Earnings, Annual Results, Special Announcement) |
| Earnings Release Date | Date when the financial results were officially released |

### Participants

| Field | Description |
|-------|-------------|
| Executive Participants | List of company executives on the call with their titles |
| CEO Presence | Whether the Chief Executive Officer participated in the call |
| CFO Presence | Whether the Chief Financial Officer participated in the call |
| Other C-Suite | Other executive officers participating (e.g., COO, CTO, CMO) |
| Call Host | Person who moderated or led the earnings call |
| Analyst Participants | List of financial analysts who asked questions |
| Analyst Firms | Investment banks or research firms represented on the call |
| Total Analyst Count | Number of analysts who asked questions during the call |

### Financial Performance Highlights

| Field | Description |
|-------|-------------|
| Revenue | Total revenue figures mentioned for the reporting period |
| Revenue Growth | Year-over-year or quarter-over-quarter revenue growth rate |
| Adjusted Revenue | Non-GAAP revenue figures if provided |
| Net Income | Profit after all expenses for the reporting period |
| Earnings Per Share (EPS) | Reported earnings per share figures |
| Adjusted EPS | Non-GAAP earnings per share figures |
| Gross Margin | Gross profit as a percentage of revenue |
| Operating Margin | Operating income as a percentage of revenue |
| Free Cash Flow | Operating cash flow minus capital expenditures |
| EBITDA | Earnings Before Interest, Taxes, Depreciation, and Amortization |
| Return Metrics | ROE, ROA, ROIC, or other return metrics mentioned |
| Beat/Miss Status | Whether results exceeded, met, or fell short of analyst expectations |

### Business Segment Performance

| Field | Description |
|-------|-------------|
| Segment Revenue | Revenue figures broken down by business segment |
| Segment Growth | Growth rates for specific business segments |
| Segment Margin | Profit margins for specific business segments |
| Geographic Breakdown | Performance details by geographic region |
| Product Line Performance | Sales or growth figures for specific product lines |
| New Product Contribution | Revenue or growth attributed to newly launched products |
| Customer Metrics | Customer acquisition, retention, or churn rates |
| Unit Economics | Cost and revenue metrics per user or unit |

### Operational Metrics

| Field | Description |
|-------|-------------|
| User Metrics | Active users, subscribers, or membership figures |
| User Growth | Growth in user base over specified periods |
| Engagement Metrics | User engagement statistics (e.g., time spent, interaction rates) |
| Conversion Rates | Metrics on user conversion through sales funnels |
| Cost Metrics | Cost of customer acquisition, production costs, etc. |
| Efficiency Ratios | Metrics measuring operational efficiency |
| Capacity Utilization | Production capacity usage rates |
| Supply Chain Metrics | Metrics related to inventory, supplies, or distribution |
| Headcount | Employee count or workforce size |

### Forward-Looking Information

| Field | Description |
|-------|-------------|
| Revenue Guidance | Management's revenue projections for future periods |
| EPS Guidance | Management's earnings per share projections |
| Growth Projections | Expected growth rates for key metrics |
| Margin Forecasts | Projected profit margin trends |
| Capital Expenditure Plans | Planned investment in physical assets |
| R&D Investment Plans | Projected spending on research and development |
| New Product Roadmap | Timeline for upcoming product or service launches |
| Market Expansion Plans | Plans to enter new markets or regions |
| Long-term Targets | Multi-year financial or operational goals |

### Strategic Initiatives

| Field | Description |
|-------|-------------|
| Strategic Priorities | Key strategic focus areas highlighted by management |
| Digital Transformation | Initiatives related to technology adoption or digital capabilities |
| Cost-cutting Measures | Programs to reduce costs or improve efficiency |
| Innovation Initiatives | New technologies or approaches being developed |
| Partnerships | New or significant business partnerships or collaborations |
| Competitive Positioning | Statements about market position relative to competitors |
| Restructuring Plans | Organizational changes or business model adjustments |
| ESG Initiatives | Environmental, social, and governance programs |

### Market Conditions & External Factors

| Field | Description |
|-------|-------------|
| Industry Trends | Broader market or industry trends affecting the business |
| Macroeconomic Commentary | Comments on general economic conditions |
| Regulatory Environment | Discussion of regulatory changes or compliance |
| Competitive Landscape | Commentary on competitor actions or market dynamics |
| Supply Chain Issues | Challenges or improvements in the supply chain |
| Consumer Behavior | Changes in customer preferences or purchasing patterns |
| Geographic Challenges | Region-specific issues affecting business |
| Currency Impacts | Effects of foreign exchange movements |

### Risk Factors & Challenges

| Field | Description |
|-------|-------------|
| Identified Risks | Specific risk factors highlighted during the call |
| Operational Challenges | Issues affecting day-to-day business operations |
| Financial Concerns | Concerns related to financial performance or structure |
| Competitive Threats | Challenges posed by market competitors |
| Regulatory Headwinds | Difficulties arising from regulatory environment |
| Margin Pressures | Factors negatively impacting profit margins |
| Litigation Updates | Information about ongoing or potential legal proceedings |
| Execution Risks | Challenges in implementing strategic initiatives |

### Analyst Interaction

| Field | Description |
|-------|-------------|
| Question Topics | Main topics covered in analyst questions |
| Recurring Questions | Themes that multiple analysts inquired about |
| Management Responses | Key points in management's answers to questions |
| Pushback Areas | Topics where analysts challenged management assertions |
| Unanswered Questions | Questions management declined to answer fully |
| Follow-up Questions | Additional questions prompted by initial responses |
| Most Active Analysts | Analysts who asked the most or most pointed questions |
| Tone of Exchange | General sentiment of the Q&A interaction |

### Tone & Sentiment

| Field | Description |
|-------|-------------|
| Management Confidence | Level of confidence expressed by executives |
| Positive Language | Frequency of positive terms or optimistic statements |
| Negative Language | Frequency of negative terms or cautious statements |
| Surprise Elements | Unexpected information or developments mentioned |
| Hedging Language | Use of qualifying or non-committal language |
| Emphasized Topics | Subjects management repeatedly stressed |
| Defensive Responses | Instances where management defended against criticism |
| Apologetic Tone | Acknowledgment of disappointments or shortfalls |

### Corporate Actions

| Field | Description |
|-------|-------------|
| Dividend Announcements | Information about dividend payments or changes |
| Share Repurchases | Stock buyback programs or activities |
| M&A Activity | Mergers, acquisitions, or divestiture announcements |
| Capital Allocation | How the company plans to deploy capital |
| Debt Management | Plans regarding company debt levels |
| Organizational Changes | Leadership transitions or restructuring |
| Special Situations | Unusual events affecting company operations |
| Investor Day Announcements | Upcoming investor events or presentations |

*Note: Not all earnings call transcripts will contain all of these fields. The availability and depth of information depends on the company's disclosure practices, industry norms, analyst participation, and the specific topics discussed during each call.*


## Documentation

For comprehensive documentation on using Earnings Transcripts capabilities, please visit our official documentation at:
[https://docs.octagonagents.com](https://docs.octagonagents.com)

Specifically for the Transcripts Agent: [Transcripts Agent Guide](https://docs.octagonagents.com/guide/agents/transcripts-agent.html)

The documentation includes:
- Detailed API references
- Transcript analysis methodology guidelines
- Examples and use cases
- Best practices for earnings call analysis
- Advanced features and capabilities

## Available Tool

### octagon-transcripts-agent
Comprehensive earnings call transcript analysis across over 8,000 public companies.

The tool uses a single `prompt` parameter that accepts a natural language query. Include all relevant details in your prompt for optimal results.

## 📚 Example Earnings Transcript Queries

### Executive Commentary Analysis
- "What did Apple's CEO say about iPhone sales trends in the latest earnings call?"
- "Summarize Tim Cook's comments on Apple's AI strategy from the Q1 2024 earnings call"
- "Extract all statements from Netflix's CEO about content strategy in international markets"
- "What did Tesla's Elon Musk say about Full Self-Driving progress in the recent earnings call?"

### Financial Guidance Extraction
- "Extract Amazon's revenue guidance for Q4 2024 from their latest earnings call"
- "What financial projections did Microsoft provide for Azure growth in their earnings call?"
- "Summarize Google's capex guidance and management's explanation for the investment levels"
- "What did Meta's CFO say about metaverse investment timeline and expected returns?"

### Analyst Questions & Interactions
- "What questions did analysts ask about Tesla's margins and how did management respond?"
- "Summarize analyst concerns about Netflix's subscriber growth and management's responses"
- "What were the most challenging questions asked during Amazon's Q3 earnings call?"
- "Extract all analyst questions about Apple's Services revenue growth sustainability"

### Business Segment Performance
- "Extract all commentary about AWS performance from Amazon's latest earnings call"
- "What did Microsoft management say about Teams and Office 365 user growth?"
- "Summarize Tesla's energy business discussion from their most recent earnings call"
- "What details did Apple provide about their wearables and services segments?"

### Competitive Landscape & Market Position
- "What did Netflix management say about competition from Disney+ and other streaming services?"
- "Extract Google's comments about AI competition with Microsoft and OpenAI"
- "What did Apple's executives say about iPhone market share in China?"
- "Summarize Tesla's discussion of EV market competition and pricing strategies"

### Operational Metrics & KPIs
- "Extract all user growth metrics mentioned in Meta's latest earnings call"
- "What operational efficiency improvements did Amazon discuss in their earnings call?"
- "Summarize Netflix's content spend and engagement metrics from the Q2 call"
- "What did Microsoft say about their cloud capacity and expansion plans?"

### Risk Factors & Challenges
- "What supply chain challenges did Apple management discuss in their earnings call?"
- "Extract all regulatory concerns mentioned in Google's latest earnings call"
- "What did Tesla management say about production bottlenecks and manufacturing issues?"
- "Summarize Netflix's discussion of content cost inflation and competitive pressures"

### Forward-Looking Statements
- "Extract all forward-looking statements about Amazon's logistics and fulfillment investments"
- "What did Microsoft management say about their AI product roadmap and timeline?"
- "Summarize Apple's commentary on future product launches and innovation pipeline"
- "What long-term targets did Tesla provide for vehicle production and energy business?"

### Sentiment & Tone Analysis
- "Analyze the tone of Meta's management when discussing metaverse investments"
- "What was the sentiment around Netflix's password sharing crackdown discussion?"
- "How confident did Apple's management sound about their India market strategy?"
- "Assess the management tone regarding Tesla's autonomous driving timeline"

### Cross-Call Comparisons
- "Compare Apple's iPhone revenue guidance between Q1 and Q2 2024 earnings calls"
- "How has Netflix's messaging about ad-tier growth evolved over the past 3 earnings calls?"
- "Track changes in Amazon's commentary about AWS growth rates over the past year"
- "Compare Tesla's production guidance consistency across the last 4 earnings calls"

## 🔍 Transcript Analysis Capabilities

- **Executive Statement Extraction**: Comprehensive analysis of C-suite commentary and strategic statements
- **Financial Guidance Analysis**: Detailed extraction of forward-looking financial projections
- **Analyst Interaction Mapping**: Complete analysis of Q&A sessions and management responses
- **Sentiment Tracking**: Advanced sentiment analysis of management tone and confidence levels
- **Trend Identification**: Long-term trend analysis across multiple earnings cycles
- **Competitive Intelligence**: Extraction of competitive positioning and market commentary
- **Risk Assessment**: Comprehensive analysis of disclosed risks and management concerns
- **Operational Insights**: Deep dive into operational metrics and efficiency discussions

## Troubleshooting

1. **API Key Issues**: Ensure your Octagon API key is correctly set in the environment or config file.
2. **Connection Issues**: Make sure the connectivity to the Octagon API is working properly.
3. **Rate Limiting**: No rate limits apply to Earnings Transcripts MCP - execute unlimited queries.

## License

MIT 

---

⭐ Star this repo if you find it helpful for your earnings analysis needs!
