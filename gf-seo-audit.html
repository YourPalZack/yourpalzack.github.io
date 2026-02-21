<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SEO Audit Dashboard - groundfloor.com</title>
    <script src="https://cdn.jsdelivr.net/npm/chart.js@4.5.1" integrity="sha384-jb8JQMbMoBUzgWatfe6COACi2ljcDdZQ2OxczGA3bGNeWe+6DChMTBJemed7ZnvJ" crossorigin="anonymous"></script>
    <style>
        *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
        :root {
            --blue: #1565C0;
            --blue-light: #E3F2FD;
            --blue-dark: #0D47A1;
            --green: #2E7D32;
            --green-light: #E8F5E9;
            --red: #C62828;
            --red-light: #FFEBEE;
            --orange: #E65100;
            --orange-light: #FFF3E0;
            --gray-50: #FAFAFA;
            --gray-100: #F5F5F5;
            --gray-200: #EEEEEE;
            --gray-300: #E0E0E0;
            --gray-400: #BDBDBD;
            --gray-600: #757575;
            --gray-700: #616161;
            --gray-800: #424242;
            --gray-900: #212121;
            --white: #FFFFFF;
            --shadow-sm: 0 1px 3px rgba(0,0,0,0.08);
            --shadow-md: 0 4px 12px rgba(0,0,0,0.1);
            --radius: 10px;
        }
        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
            background: var(--gray-100);
            color: var(--gray-900);
            line-height: 1.5;
            -webkit-font-smoothing: antialiased;
        }
        .dashboard {
            max-width: 1400px;
            margin: 0 auto;
            padding: 24px;
        }
        header {
            display: flex;
            justify-content: space-between;
            align-items: flex-start;
            margin-bottom: 28px;
            flex-wrap: wrap;
            gap: 16px;
        }
        header .title-group h1 {
            font-size: 26px;
            font-weight: 700;
            color: var(--gray-900);
            letter-spacing: -0.3px;
        }
        header .title-group p {
            font-size: 14px;
            color: var(--gray-600);
            margin-top: 4px;
        }
        .nav-tabs {
            display: flex;
            gap: 4px;
            background: var(--white);
            border-radius: 8px;
            padding: 4px;
            box-shadow: var(--shadow-sm);
        }
        .nav-tab {
            padding: 8px 18px;
            border-radius: 6px;
            border: none;
            background: transparent;
            font-size: 13px;
            font-weight: 500;
            color: var(--gray-600);
            cursor: pointer;
            transition: all 0.2s;
        }
        .nav-tab:hover { color: var(--gray-900); background: var(--gray-100); }
        .nav-tab.active { background: var(--blue); color: var(--white); }
        .section { display: none; }
        .section.active { display: block; }

        /* KPI Cards */
        .kpi-row {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 16px;
            margin-bottom: 24px;
        }
        .kpi-card {
            background: var(--white);
            border-radius: var(--radius);
            padding: 20px 22px;
            box-shadow: var(--shadow-sm);
            border-left: 4px solid var(--blue);
            transition: box-shadow 0.2s;
        }
        .kpi-card:hover { box-shadow: var(--shadow-md); }
        .kpi-card.green { border-left-color: var(--green); }
        .kpi-card.red { border-left-color: var(--red); }
        .kpi-card.orange { border-left-color: var(--orange); }
        .kpi-label {
            font-size: 12px;
            font-weight: 600;
            text-transform: uppercase;
            letter-spacing: 0.5px;
            color: var(--gray-600);
            margin-bottom: 6px;
        }
        .kpi-value {
            font-size: 28px;
            font-weight: 700;
            color: var(--gray-900);
            line-height: 1.1;
        }
        .kpi-sub {
            font-size: 13px;
            margin-top: 6px;
            display: flex;
            align-items: center;
            gap: 4px;
        }
        .kpi-sub.positive { color: var(--green); }
        .kpi-sub.negative { color: var(--red); }
        .kpi-sub.neutral { color: var(--gray-600); }

        /* Score gauge */
        .score-section {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 20px;
            margin-bottom: 24px;
        }
        .score-card {
            background: var(--white);
            border-radius: var(--radius);
            padding: 28px;
            box-shadow: var(--shadow-sm);
            text-align: center;
        }
        .score-card h3 {
            font-size: 14px;
            font-weight: 600;
            color: var(--gray-600);
            text-transform: uppercase;
            letter-spacing: 0.5px;
            margin-bottom: 12px;
        }
        .score-ring {
            position: relative;
            width: 140px;
            height: 140px;
            margin: 0 auto 12px;
        }
        .score-ring canvas { width: 140px !important; height: 140px !important; }
        .score-number {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            font-size: 36px;
            font-weight: 800;
        }
        .score-number.low { color: var(--red); }
        .score-number.high { color: var(--green); }

        /* Charts */
        .chart-row {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 20px;
            margin-bottom: 24px;
        }
        .chart-row.full { grid-template-columns: 1fr; }
        .chart-card {
            background: var(--white);
            border-radius: var(--radius);
            padding: 24px;
            box-shadow: var(--shadow-sm);
        }
        .chart-card h3 {
            font-size: 15px;
            font-weight: 600;
            color: var(--gray-800);
            margin-bottom: 16px;
        }
        .chart-container { position: relative; width: 100%; }

        /* Tables */
        .table-card {
            background: var(--white);
            border-radius: var(--radius);
            padding: 24px;
            box-shadow: var(--shadow-sm);
            margin-bottom: 24px;
            overflow-x: auto;
        }
        .table-card h3 {
            font-size: 15px;
            font-weight: 600;
            color: var(--gray-800);
            margin-bottom: 16px;
        }
        table {
            width: 100%;
            border-collapse: collapse;
            font-size: 13px;
        }
        thead th {
            background: var(--gray-50);
            padding: 10px 14px;
            text-align: left;
            font-weight: 600;
            color: var(--gray-700);
            border-bottom: 2px solid var(--gray-200);
            cursor: pointer;
            white-space: nowrap;
            user-select: none;
        }
        thead th:hover { background: var(--gray-200); }
        thead th .sort-arrow { margin-left: 4px; opacity: 0.3; }
        thead th.sorted .sort-arrow { opacity: 1; }
        tbody td {
            padding: 10px 14px;
            border-bottom: 1px solid var(--gray-200);
            white-space: nowrap;
        }
        tbody tr:hover { background: var(--blue-light); }
        .badge {
            display: inline-block;
            padding: 2px 8px;
            border-radius: 4px;
            font-size: 11px;
            font-weight: 600;
        }
        .badge-green { background: var(--green-light); color: var(--green); }
        .badge-red { background: var(--red-light); color: var(--red); }
        .badge-orange { background: var(--orange-light); color: var(--orange); }
        .badge-blue { background: var(--blue-light); color: var(--blue); }
        .winner-cell { font-weight: 600; }
        .winner-gf { color: var(--green); }
        .winner-comp { color: var(--red); }

        /* Action Plan */
        .action-card {
            background: var(--white);
            border-radius: var(--radius);
            padding: 20px 24px;
            box-shadow: var(--shadow-sm);
            margin-bottom: 12px;
            display: grid;
            grid-template-columns: 36px 1fr auto auto;
            align-items: center;
            gap: 16px;
        }
        .action-number {
            width: 36px;
            height: 36px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: 700;
            font-size: 14px;
            color: var(--white);
        }
        .action-number.immediate { background: var(--red); }
        .action-number.short { background: var(--orange); }
        .action-number.medium { background: var(--blue); }
        .action-number.long { background: var(--gray-600); }
        .action-content h4 { font-size: 14px; font-weight: 600; color: var(--gray-900); }
        .action-content p { font-size: 12px; color: var(--gray-600); margin-top: 2px; }
        .action-effort, .action-impact {
            font-size: 11px;
            font-weight: 600;
            padding: 4px 10px;
            border-radius: 4px;
        }
        .effort-low { background: var(--green-light); color: var(--green); }
        .effort-med { background: var(--orange-light); color: var(--orange); }
        .effort-high { background: var(--red-light); color: var(--red); }
        .impact-high { background: #E8F5E9; color: #1B5E20; }
        .impact-med { background: #FFF3E0; color: #BF360C; }
        .impact-low { background: #F5F5F5; color: #616161; }

        /* Projections */
        .projection-row {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 20px;
            margin-bottom: 24px;
        }
        .projection-card {
            background: var(--white);
            border-radius: var(--radius);
            padding: 24px;
            box-shadow: var(--shadow-sm);
        }
        .projection-card h3 { font-size: 15px; font-weight: 600; margin-bottom: 12px; }
        .projection-card.conservative { border-top: 4px solid var(--blue); }
        .projection-card.optimistic { border-top: 4px solid var(--green); }
        .projection-value { font-size: 32px; font-weight: 800; margin-bottom: 4px; }
        .projection-card.conservative .projection-value { color: var(--blue); }
        .projection-card.optimistic .projection-value { color: var(--green); }

        /* Content gap cards */
        .gap-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 16px;
            margin-bottom: 24px;
        }
        .gap-card {
            background: var(--white);
            border-radius: var(--radius);
            padding: 20px;
            box-shadow: var(--shadow-sm);
            border-top: 3px solid var(--blue);
        }
        .gap-card h4 { font-size: 14px; font-weight: 600; margin-bottom: 8px; color: var(--gray-900); }
        .gap-meta { display: flex; gap: 12px; flex-wrap: wrap; margin-bottom: 8px; }
        .gap-meta span { font-size: 12px; color: var(--gray-600); }
        .gap-meta strong { color: var(--gray-900); }
        .gap-card p { font-size: 13px; color: var(--gray-700); line-height: 1.5; }

        .section-title {
            font-size: 13px;
            font-weight: 700;
            text-transform: uppercase;
            letter-spacing: 0.8px;
            color: var(--gray-600);
            margin-bottom: 16px;
            padding-bottom: 8px;
            border-bottom: 2px solid var(--gray-200);
        }

        .insight-box {
            background: var(--blue-light);
            border-left: 4px solid var(--blue);
            border-radius: 0 var(--radius) var(--radius) 0;
            padding: 16px 20px;
            margin-bottom: 24px;
            font-size: 14px;
            color: var(--gray-800);
            line-height: 1.6;
        }

        @media (max-width: 900px) {
            .chart-row, .score-section, .projection-row { grid-template-columns: 1fr; }
            .action-card { grid-template-columns: 36px 1fr; }
            .action-effort, .action-impact { grid-column: 2; }
            header { flex-direction: column; }
        }
        @media print {
            body { background: white; }
            .nav-tabs { display: none; }
            .section { display: block !important; page-break-inside: avoid; }
        }
    </style>
</head>
<body>
<div class="dashboard">
    <header>
        <div class="title-group">
            <h1>SEO Audit Dashboard</h1>
            <p>groundfloor.com | February 20, 2026 | Benchmarked vs. Fundrise.com</p>
        </div>
        <nav class="nav-tabs">
            <button class="nav-tab active" data-tab="overview">Overview</button>
            <button class="nav-tab" data-tab="keywords">Keywords</button>
            <button class="nav-tab" data-tab="competitors">Competitors</button>
            <button class="nav-tab" data-tab="content">Content Gaps</button>
            <button class="nav-tab" data-tab="backlinks">Backlinks</button>
            <button class="nav-tab" data-tab="actions">Action Plan</button>
        </nav>
    </header>

    <!-- ============ OVERVIEW ============ -->
    <div id="overview" class="section active">
        <div class="score-section">
            <div class="score-card">
                <h3>Groundfloor Visibility Score</h3>
                <div class="score-ring">
                    <canvas id="scoreGF"></canvas>
                    <div class="score-number low">20</div>
                </div>
                <p style="font-size:13px;color:var(--gray-600);">Significant room for growth</p>
            </div>
            <div class="score-card">
                <h3>Fundrise Visibility Score</h3>
                <div class="score-ring">
                    <canvas id="scoreFR"></canvas>
                    <div class="score-number high">74</div>
                </div>
                <p style="font-size:13px;color:var(--gray-600);">Strong organic presence</p>
            </div>
        </div>

        <div class="insight-box">
            The 54-point visibility gap is driven almost entirely by content coverage and non-branded keyword targeting. 88% of Groundfloor's organic traffic comes from people who already know the brand. Fundrise captures tens of thousands of visitors monthly through educational content about real estate investing, crowdfunding comparisons, and investment guides. The gap is a content execution problem, not an authority problem - Groundfloor has strong backlinks from Apple, Bloomberg, and Investopedia.
        </div>

        <div class="kpi-row">
            <div class="kpi-card red">
                <div class="kpi-label">Organic Traffic</div>
                <div class="kpi-value">8,206</div>
                <div class="kpi-sub negative">-27% vs 12 months ago</div>
            </div>
            <div class="kpi-card">
                <div class="kpi-label">Domain Rating</div>
                <div class="kpi-value">49</div>
                <div class="kpi-sub positive">+2 pts in 6 months</div>
            </div>
            <div class="kpi-card orange">
                <div class="kpi-label">Organic Keywords</div>
                <div class="kpi-value">677</div>
                <div class="kpi-sub negative">3.6x fewer than Fundrise</div>
            </div>
            <div class="kpi-card green">
                <div class="kpi-label">Referring Domains</div>
                <div class="kpi-value">1,253</div>
                <div class="kpi-sub positive">+27% in 6 months</div>
            </div>
            <div class="kpi-card red">
                <div class="kpi-label">Branded Traffic %</div>
                <div class="kpi-value">88%</div>
                <div class="kpi-sub negative">Target: below 60%</div>
            </div>
            <div class="kpi-card">
                <div class="kpi-label">Traffic Value</div>
                <div class="kpi-value">$739K</div>
                <div class="kpi-sub neutral">vs Fundrise $13.9M</div>
            </div>
        </div>

        <div class="chart-row">
            <div class="chart-card">
                <h3>Organic Traffic - 12 Month Trend</h3>
                <div class="chart-container"><canvas id="trafficTrend"></canvas></div>
            </div>
            <div class="chart-card">
                <h3>Referring Domains - 6 Month Trend</h3>
                <div class="chart-container"><canvas id="refdomainsTrend"></canvas></div>
            </div>
        </div>

        <div class="chart-row">
            <div class="chart-card">
                <h3>Visibility Score Breakdown</h3>
                <div class="chart-container"><canvas id="scoreBreakdown"></canvas></div>
            </div>
            <div class="chart-card">
                <h3>Traffic Composition</h3>
                <div class="chart-container"><canvas id="trafficComposition"></canvas></div>
            </div>
        </div>
    </div>

    <!-- ============ KEYWORDS ============ -->
    <div id="keywords" class="section">
        <div class="kpi-row">
            <div class="kpi-card">
                <div class="kpi-label">Total Keywords</div>
                <div class="kpi-value">677</div>
                <div class="kpi-sub neutral">Fundrise: 2,445</div>
            </div>
            <div class="kpi-card green">
                <div class="kpi-label">Top 3 Positions</div>
                <div class="kpi-value">107</div>
                <div class="kpi-sub neutral">15.8% of portfolio</div>
            </div>
            <div class="kpi-card">
                <div class="kpi-label">Top 4-10 Positions</div>
                <div class="kpi-value">207</div>
                <div class="kpi-sub neutral">30.6% of portfolio</div>
            </div>
            <div class="kpi-card orange">
                <div class="kpi-label">Striking Distance (4-15)</div>
                <div class="kpi-value">6</div>
                <div class="kpi-sub neutral">Non-branded, high volume</div>
            </div>
        </div>

        <div class="chart-row">
            <div class="chart-card">
                <h3>Keyword Position Distribution</h3>
                <div class="chart-container"><canvas id="kwPositions"></canvas></div>
            </div>
            <div class="chart-card">
                <h3>Top Keywords by Traffic</h3>
                <div class="chart-container"><canvas id="kwTraffic"></canvas></div>
            </div>
        </div>

        <div class="table-card">
            <h3>Top Organic Keywords</h3>
            <table id="kwTable">
                <thead>
                    <tr>
                        <th onclick="sortTable('kwTable',0)">Keyword <span class="sort-arrow">&#9650;</span></th>
                        <th onclick="sortTable('kwTable',1)">Volume <span class="sort-arrow">&#9650;</span></th>
                        <th onclick="sortTable('kwTable',2)">Position <span class="sort-arrow">&#9650;</span></th>
                        <th onclick="sortTable('kwTable',3)">Traffic <span class="sort-arrow">&#9650;</span></th>
                        <th onclick="sortTable('kwTable',4)">KD <span class="sort-arrow">&#9650;</span></th>
                        <th onclick="sortTable('kwTable',5)">Intent</th>
                        <th>Page</th>
                    </tr>
                </thead>
                <tbody></tbody>
            </table>
        </div>

        <div class="insight-box">
            Striking distance keywords are your quickest wins. "Crowdfunding real estate" (1,100 volume, position 11), "how to see who bought a house" (1,000 volume, position 12), and "do you need a real estate license to flip houses" (350 volume, position 8) could each move into the top 5 with content improvements and internal linking.
        </div>
    </div>

    <!-- ============ COMPETITORS ============ -->
    <div id="competitors" class="section">
        <p class="section-title">Head-to-Head: Groundfloor vs Fundrise</p>
        <div class="table-card">
            <h3>Domain Authority and Link Profile</h3>
            <table>
                <thead>
                    <tr><th>Metric</th><th>Groundfloor</th><th>Fundrise</th><th>Delta</th><th>Winner</th></tr>
                </thead>
                <tbody>
                    <tr><td>Domain Rating</td><td>49</td><td>73</td><td style="color:var(--red)">-24</td><td class="winner-cell winner-comp">Fundrise</td></tr>
                    <tr><td>Ahrefs Rank</td><td>735,985</td><td>59,081</td><td style="color:var(--red)">-</td><td class="winner-cell winner-comp">Fundrise</td></tr>
                    <tr><td>Live Backlinks</td><td>26,780</td><td>46,820</td><td style="color:var(--red)">-20,040</td><td class="winner-cell winner-comp">Fundrise</td></tr>
                    <tr><td>Live Referring Domains</td><td>1,253</td><td>4,393</td><td style="color:var(--red)">-3,140</td><td class="winner-cell winner-comp">Fundrise</td></tr>
                    <tr><td>DR Trend (6mo)</td><td>47 to 49 (+2)</td><td>Stable ~73</td><td style="color:var(--green)">Improving</td><td class="winner-cell winner-gf">Groundfloor</td></tr>
                    <tr><td>Refdomains Trend (6mo)</td><td>+27%</td><td>-6.5%</td><td style="color:var(--green)">Growing</td><td class="winner-cell winner-gf">Groundfloor</td></tr>
                </tbody>
            </table>
        </div>

        <div class="table-card">
            <h3>Organic Search Performance</h3>
            <table>
                <thead>
                    <tr><th>Metric</th><th>Groundfloor</th><th>Fundrise</th><th>Delta</th><th>Winner</th></tr>
                </thead>
                <tbody>
                    <tr><td>Organic Traffic (monthly)</td><td>8,206</td><td>55,572</td><td style="color:var(--red)">-47,366</td><td class="winner-cell winner-comp">Fundrise</td></tr>
                    <tr><td>Organic Keywords</td><td>677</td><td>2,445</td><td style="color:var(--red)">-1,768</td><td class="winner-cell winner-comp">Fundrise</td></tr>
                    <tr><td>Keywords in Top 3</td><td>107</td><td>608</td><td style="color:var(--red)">-501</td><td class="winner-cell winner-comp">Fundrise</td></tr>
                    <tr><td>Keywords in Top 4-10</td><td>207</td><td>843</td><td style="color:var(--red)">-636</td><td class="winner-cell winner-comp">Fundrise</td></tr>
                    <tr><td>Traffic Value ($/mo)</td><td>$739,477</td><td>$13,910,076</td><td style="color:var(--red)">-$13.2M</td><td class="winner-cell winner-comp">Fundrise</td></tr>
                    <tr><td>Traffic Trend (12mo)</td><td>-27%</td><td>-31%</td><td style="color:var(--green)">Less decline</td><td class="winner-cell winner-gf">Groundfloor</td></tr>
                </tbody>
            </table>
        </div>

        <div class="chart-row">
            <div class="chart-card">
                <h3>Traffic Comparison - 12 Months</h3>
                <div class="chart-container"><canvas id="compTraffic"></canvas></div>
            </div>
            <div class="chart-card">
                <h3>Keyword Coverage Comparison</h3>
                <div class="chart-container"><canvas id="compKeywords"></canvas></div>
            </div>
        </div>

        <div class="table-card">
            <h3>Top 10 Organic Competitors by Keyword Overlap</h3>
            <table id="compTable">
                <thead>
                    <tr>
                        <th>Competitor</th><th>Common KWs</th><th>Their KWs</th><th>Traffic</th><th>DR</th><th>Share</th>
                    </tr>
                </thead>
                <tbody>
                    <tr><td>groundfloor.us</td><td>47</td><td>19</td><td>700</td><td>51</td><td><span class="badge badge-green">22.3%</span></td></tr>
                    <tr><td>kiavi.com</td><td>146</td><td>1,414</td><td>20,069</td><td>60</td><td><span class="badge badge-blue">6.9%</span></td></tr>
                    <tr><td>dominionfinancialservices.com</td><td>64</td><td>510</td><td>3,052</td><td>32</td><td><span class="badge badge-blue">5.5%</span></td></tr>
                    <tr><td>easystreetcap.com</td><td>89</td><td>968</td><td>8,271</td><td>46</td><td><span class="badge badge-blue">5.4%</span></td></tr>
                    <tr><td>limaone.com</td><td>72</td><td>1,051</td><td>8,868</td><td>51</td><td><span class="badge badge-blue">4.1%</span></td></tr>
                    <tr><td>rehabfinancial.com</td><td>53</td><td>663</td><td>4,028</td><td>40</td><td><span class="badge badge-blue">4.0%</span></td></tr>
                    <tr><td>realtymogul.com</td><td>79</td><td>1,477</td><td>9,455</td><td>64</td><td><span class="badge badge-blue">3.6%</span></td></tr>
                    <tr><td>fundrise.com</td><td>107</td><td>2,338</td><td>55,572</td><td>73</td><td><span class="badge badge-orange">3.5%</span></td></tr>
                    <tr><td>arrived.com</td><td>98</td><td>2,911</td><td>20,901</td><td>54</td><td><span class="badge badge-blue">2.7%</span></td></tr>
                    <tr><td>equitymultiple.com</td><td>63</td><td>2,194</td><td>18,247</td><td>55</td><td><span class="badge badge-blue">2.1%</span></td></tr>
                </tbody>
            </table>
        </div>

        <div class="insight-box">
            The competitive landscape splits into two tiers. Direct lending competitors (Kiavi, Lima One, EasyStreet) compete in hard money lending and fix-and-flip content. Investment platform competitors (Fundrise, Arrived, RealtyMogul, EquityMultiple) compete on real estate investing education. Groundfloor uniquely straddles both markets but has built almost no content for either. This is both the biggest problem and the biggest opportunity.
        </div>
    </div>

    <!-- ============ CONTENT GAPS ============ -->
    <div id="content" class="section">
        <p class="section-title">Content Gap Opportunities</p>
        <div class="insight-box">
            These are high-value keywords that Fundrise and other competitors rank for, but Groundfloor does not. Each represents a content opportunity that could drive meaningful non-branded traffic. The list is ordered by a combination of search volume, keyword difficulty, and relevance to Groundfloor's business.
        </div>

        <div class="gap-grid">
            <div class="gap-card">
                <h4>Real Estate Investing for Beginners</h4>
                <div class="gap-meta">
                    <span>Volume: <strong>5,200</strong></span>
                    <span>KD: <strong>35</strong></span>
                    <span>Est. Traffic: <strong>500-1,500/mo</strong></span>
                </div>
                <p>Create a 3,000-4,000 word comprehensive guide covering types of real estate investments (direct ownership, REITs, crowdfunding, notes), how to get started with little money, risk vs reward. Target URL: /blog/real-estate-investing-for-beginners</p>
            </div>
            <div class="gap-card">
                <h4>Real Estate Crowdfunding Platforms Compared</h4>
                <div class="gap-meta">
                    <span>Volume: <strong>1,800</strong></span>
                    <span>KD: <strong>72</strong></span>
                    <span>Est. Traffic: <strong>300-800/mo</strong></span>
                </div>
                <p>3,000-4,000 word comparison article covering Groundfloor, Fundrise, Arrived, RealtyMogul, and EquityMultiple. Include honest pros/cons, minimum investments, returns data, and fee structures. Target: /blog/best-real-estate-crowdfunding-platforms</p>
            </div>
            <div class="gap-card">
                <h4>Fractional Real Estate Investing</h4>
                <div class="gap-meta">
                    <span>Volume: <strong>800</strong></span>
                    <span>KD: <strong>21</strong></span>
                    <span>Est. Traffic: <strong>200-400/mo</strong></span>
                </div>
                <p>2,000-2,500 word explainer covering how fractional ownership works, platforms available, pros and cons, and how it compares to REITs and crowdfunding. Target: /education-hub/fractional-real-estate-investing</p>
            </div>
            <div class="gap-card">
                <h4>Passive Real Estate Investing</h4>
                <div class="gap-meta">
                    <span>Volume: <strong>600</strong></span>
                    <span>KD: <strong>28</strong></span>
                    <span>Est. Traffic: <strong>150-300/mo</strong></span>
                </div>
                <p>2,500 word guide on 7 ways to earn passive income from real estate without being a landlord. Position Groundfloor's LROs and notes as key options alongside REITs, syndications, and crowdfunding. Target: /blog/passive-real-estate-investing</p>
            </div>
            <div class="gap-card">
                <h4>What is Real Estate Crowdfunding?</h4>
                <div class="gap-meta">
                    <span>Volume: <strong>500</strong></span>
                    <span>KD: <strong>1</strong></span>
                    <span>Est. Traffic: <strong>200-500/mo</strong></span>
                </div>
                <p>Nearly guaranteed to rank quickly at KD 1. Create a 2,500-3,000 word educational page explaining crowdfunding, how it works, risks, returns history, and regulatory framework. This should be the first content priority. Target: /education-hub/what-is-real-estate-crowdfunding</p>
            </div>
            <div class="gap-card">
                <h4>Real Estate Crowdfunding Returns</h4>
                <div class="gap-meta">
                    <span>Volume: <strong>200</strong></span>
                    <span>KD: <strong>7</strong></span>
                    <span>Est. Traffic: <strong>80-150/mo</strong></span>
                </div>
                <p>Create a data-driven page showcasing historical returns across real estate crowdfunding platforms. Groundfloor's actual performance data is a competitive advantage here. Target: /education-hub/real-estate-crowdfunding-returns</p>
            </div>
        </div>

        <div class="chart-row full">
            <div class="chart-card">
                <h3>Content Opportunities: Volume vs Difficulty</h3>
                <div class="chart-container"><canvas id="gapBubble"></canvas></div>
            </div>
        </div>
    </div>

    <!-- ============ BACKLINKS ============ -->
    <div id="backlinks" class="section">
        <div class="kpi-row">
            <div class="kpi-card">
                <div class="kpi-label">Live Backlinks</div>
                <div class="kpi-value">26,780</div>
                <div class="kpi-sub neutral">Fundrise: 46,820</div>
            </div>
            <div class="kpi-card green">
                <div class="kpi-label">Referring Domains</div>
                <div class="kpi-value">1,253</div>
                <div class="kpi-sub positive">+27% in 6 months</div>
            </div>
            <div class="kpi-card">
                <div class="kpi-label">High-Authority Links (DR 90+)</div>
                <div class="kpi-value">10</div>
                <div class="kpi-sub positive">Apple, Bloomberg, Investopedia</div>
            </div>
            <div class="kpi-card red">
                <div class="kpi-label">Broken Backlinks</div>
                <div class="kpi-value">9</div>
                <div class="kpi-sub negative">Quick win: fix redirects</div>
            </div>
        </div>

        <div class="chart-row">
            <div class="chart-card">
                <h3>Top Referring Domains by DR</h3>
                <div class="chart-container"><canvas id="refDomainsDR"></canvas></div>
            </div>
            <div class="chart-card">
                <h3>Referring Domains Growth vs Fundrise</h3>
                <div class="chart-container"><canvas id="refDomainsGrowth"></canvas></div>
            </div>
        </div>

        <div class="table-card">
            <h3>Broken Backlinks to Reclaim</h3>
            <table>
                <thead>
                    <tr><th>Source Page</th><th>Source DR</th><th>Broken Target</th><th>Anchor</th><th>Priority</th></tr>
                </thead>
                <tbody>
                    <tr><td>joywallet.com/.../fundrise-alternatives/</td><td>70</td><td>/investors</td><td>"the company's"</td><td><span class="badge badge-red">High</span></td></tr>
                    <tr><td>tradethatswing.com/.../alternative-investments...</td><td>51</td><td>/investors</td><td>"Groundfloor"</td><td><span class="badge badge-red">High</span></td></tr>
                    <tr><td>blog.groundfloor.us/whats-next...</td><td>51</td><td>/whats-next... (blog)</td><td>(redirect)</td><td><span class="badge badge-orange">Medium</span></td></tr>
                    <tr><td>capitalnomads.com/.../alternative-investing...</td><td>0</td><td>/investors</td><td>"Learn More"</td><td><span class="badge badge-blue">Low</span></td></tr>
                </tbody>
            </table>
        </div>

        <div class="insight-box">
            Groundfloor has an impressive high-authority backlink profile for its size. Links from Apple (DR 97), Bloomberg (DR 92), Investopedia (DR 92), and Wikipedia (DR 97) carry significant weight. The referring domain count is growing at 27% over 6 months while Fundrise's is declining. The immediate priority is setting up a 301 redirect from /investors to the appropriate current page to recover link equity from the DR 70 and DR 51 broken backlink sources.
        </div>
    </div>

    <!-- ============ ACTION PLAN ============ -->
    <div id="actions" class="section">
        <p class="section-title">Immediate Actions - Week 1-2</p>
        <div class="action-card">
            <div class="action-number immediate">1</div>
            <div class="action-content">
                <h4>Fix broken /investors redirect</h4>
                <p>Set up 301 redirect from /investors to homepage or new landing page. Recovers link equity from DR 70 and DR 51 sources.</p>
            </div>
            <span class="action-effort effort-low">1 hour</span>
            <span class="action-impact impact-med">Moderate impact</span>
        </div>
        <div class="action-card">
            <div class="action-number immediate">2</div>
            <div class="action-content">
                <h4>Optimize homepage title and meta description</h4>
                <p>Include "real estate crowdfunding" and "investing platform" in title tag. Write a compelling meta description with CTA.</p>
            </div>
            <span class="action-effort effort-low">30 min</span>
            <span class="action-impact impact-med">Moderate impact</span>
        </div>
        <div class="action-card">
            <div class="action-number immediate">3</div>
            <div class="action-content">
                <h4>Publish "What is Real Estate Crowdfunding?" article</h4>
                <p>KD 1, 500 monthly searches. Nearly guaranteed to rank quickly. First content priority.</p>
            </div>
            <span class="action-effort effort-med">4-6 hours</span>
            <span class="action-impact impact-high">High impact</span>
        </div>

        <p class="section-title" style="margin-top:28px;">Short-Term - Month 1-2</p>
        <div class="action-card">
            <div class="action-number short">4</div>
            <div class="action-content">
                <h4>Publish "Real Estate Investing for Beginners" guide</h4>
                <p>5,200 volume, KD 35. Comprehensive 3,000-4,000 word guide. Highest traffic potential of any single content piece.</p>
            </div>
            <span class="action-effort effort-med">8-12 hours</span>
            <span class="action-impact impact-high">Very high impact</span>
        </div>
        <div class="action-card">
            <div class="action-number short">5</div>
            <div class="action-content">
                <h4>Publish "Fractional Real Estate Investing" guide</h4>
                <p>800 volume, KD 21. Easy-moderate difficulty with strong commercial intent.</p>
            </div>
            <span class="action-effort effort-med">4-6 hours</span>
            <span class="action-impact impact-high">High impact</span>
        </div>
        <div class="action-card">
            <div class="action-number short">6</div>
            <div class="action-content">
                <h4>Optimize "how to find out who owns a house" blog post</h4>
                <p>Currently position 12 for a 1,000-volume keyword. Add depth, update content, improve internal links to push into top 5.</p>
            </div>
            <span class="action-effort effort-low">2-3 hours</span>
            <span class="action-impact impact-med">Moderate impact</span>
        </div>
        <div class="action-card">
            <div class="action-number short">7</div>
            <div class="action-content">
                <h4>Create /education-hub/ content hub</h4>
                <p>Central landing page for all educational content. Builds topical authority and improves internal linking structure.</p>
            </div>
            <span class="action-effort effort-med">4-6 hours</span>
            <span class="action-impact impact-med">Foundation</span>
        </div>

        <p class="section-title" style="margin-top:28px;">Medium-Term - Month 3-6</p>
        <div class="action-card">
            <div class="action-number medium">8</div>
            <div class="action-content">
                <h4>Publish "Best Real Estate Crowdfunding Platforms" comparison</h4>
                <p>1,800 volume. Honest comparison with Fundrise, Arrived, RealtyMogul. High commercial value.</p>
            </div>
            <span class="action-effort effort-med">8-12 hours</span>
            <span class="action-impact impact-high">High impact</span>
        </div>
        <div class="action-card">
            <div class="action-number medium">9</div>
            <div class="action-content">
                <h4>Launch link-building outreach campaign</h4>
                <p>Target personal finance blogs and "best real estate crowdfunding" roundup articles. Focus on closing the DR gap with Fundrise.</p>
            </div>
            <span class="action-effort effort-high">Ongoing</span>
            <span class="action-impact impact-high">High impact</span>
        </div>
        <div class="action-card">
            <div class="action-number medium">10</div>
            <div class="action-content">
                <h4>Optimize striking distance keywords</h4>
                <p>"Do you need a real estate license to flip houses" (pos 8, 350 vol), "how to invest without buying property" (pos 6, 250 vol).</p>
            </div>
            <span class="action-effort effort-low">2-3 hours each</span>
            <span class="action-impact impact-med">Moderate impact</span>
        </div>

        <p class="section-title" style="margin-top:28px;">Long-Term - Month 6-12</p>
        <div class="action-card">
            <div class="action-number long">11</div>
            <div class="action-content">
                <h4>Build complete topic clusters</h4>
                <p>Real estate investing education, fix-and-flip financing, passive income strategies, market analysis. Target 20-30 new content pieces.</p>
            </div>
            <span class="action-effort effort-high">Major</span>
            <span class="action-impact impact-high">Transformative</span>
        </div>
        <div class="action-card">
            <div class="action-number long">12</div>
            <div class="action-content">
                <h4>Develop borrower content hub on lending.groundfloor.com</h4>
                <p>Target hard money lending, fix-and-flip loans, construction loans. Untapped second front that Kiavi and Lima One dominate.</p>
            </div>
            <span class="action-effort effort-high">Major</span>
            <span class="action-impact impact-high">High impact</span>
        </div>

        <div class="projection-row" style="margin-top:32px;">
            <div class="projection-card conservative">
                <h3>Conservative 6-Month Projection</h3>
                <div class="projection-value">+1,150/mo</div>
                <p style="font-size:14px;color:var(--gray-600);">14% traffic increase to ~9,350 monthly visits</p>
                <p style="font-size:13px;color:var(--gray-600);margin-top:8px;">Based on executing top 5 content pieces and ranking in positions 5-10</p>
            </div>
            <div class="projection-card optimistic">
                <h3>Optimistic 6-Month Projection</h3>
                <div class="projection-value">+3,100/mo</div>
                <p style="font-size:14px;color:var(--gray-600);">38% traffic increase to ~11,300 monthly visits</p>
                <p style="font-size:13px;color:var(--gray-600);margin-top:8px;">Based on content + technical fixes + internal linking + link building</p>
            </div>
        </div>
    </div>
</div>

<script>
// ========== DATA ==========
const MONTHS_12 = ['Mar 25','Apr 25','May 25','Jun 25','Jul 25','Aug 25','Sep 25','Oct 25','Nov 25','Dec 25','Jan 26','Feb 26'];
const GF_TRAFFIC = [11214,10385,9954,10371,10100,10004,9525,8931,8809,8363,9437,9361];
const FR_TRAFFIC = [80094,73017,62126,69409,75013,67915,57985,51891,48841,47689,60275,60967];

const MONTHS_6 = ['Sep 25','Oct 25','Nov 25','Dec 25','Jan 26','Feb 26'];
const GF_REFDOMAINS = [982,1040,1105,1327,1333,1246];
const FR_REFDOMAINS = [4697,4789,4631,4503,4475,4393];

const KEYWORDS = [
    {kw:"groundfloor",vol:6600,pos:1,traffic:5943,kd:3,intent:"Branded",page:"Homepage"},
    {kw:"groundfloor login",vol:900,pos:1,traffic:322,kd:3,intent:"Branded",page:"Homepage"},
    {kw:"ground floor",vol:3300,pos:2,traffic:247,kd:13,intent:"Branded",page:"Homepage"},
    {kw:"lros",vol:150,pos:1,traffic:148,kd:0,intent:"Informational",page:"/lro/"},
    {kw:"groundfloor lending",vol:250,pos:1,traffic:142,kd:4,intent:"Commercial",page:"lending.groundfloor.com"},
    {kw:"groundfloor investing",vol:250,pos:1,traffic:83,kd:3,intent:"Commercial",page:"Homepage"},
    {kw:"ground floor lending",vol:150,pos:1,traffic:79,kd:4,intent:"Commercial",page:"lending.groundfloor.com"},
    {kw:"groundfloor.com",vol:60,pos:1,traffic:62,kd:3,intent:"Branded",page:"Homepage"},
    {kw:"groundfloor finance",vol:200,pos:1,traffic:59,kd:5,intent:"Branded",page:"Homepage"},
    {kw:"crowdfunding real estate",vol:1100,pos:11,traffic:22,kd:76,intent:"Commercial",page:"Homepage"},
    {kw:"how to invest in RE without buying property",vol:250,pos:6,traffic:19,kd:33,intent:"Informational",page:"Homepage"},
    {kw:"how to see who bought a house",vol:1000,pos:12,traffic:16,kd:5,intent:"Informational",page:"Blog"},
    {kw:"groundfloor review",vol:350,pos:1,traffic:25,kd:9,intent:"Commercial",page:"Homepage"},
    {kw:"do you need a RE license to flip houses",vol:350,pos:8,traffic:13,kd:0,intent:"Informational",page:"Blog"},
    {kw:"groundfloor notes",vol:60,pos:1,traffic:31,kd:0,intent:"Commercial",page:"/notes/"},
    {kw:"groundfloor stock",vol:40,pos:1,traffic:16,kd:0,intent:"Informational",page:"/education-hub/"},
    {kw:"invest in RE without buying property",vol:100,pos:4,traffic:14,kd:30,intent:"Informational",page:"Homepage"},
    {kw:"groundfloor real estate",vol:50,pos:1,traffic:20,kd:1,intent:"Branded",page:"Homepage"},
    {kw:"what is groundfloor investing",vol:30,pos:1,traffic:14,kd:2,intent:"Branded",page:"Homepage"},
    {kw:"groundfloor app",vol:60,pos:3,traffic:12,kd:2,intent:"Branded",page:"Homepage"},
    {kw:"how to make money on groundfloor",vol:40,pos:1,traffic:21,kd:0,intent:"Informational",page:"Blog"},
    {kw:"passive investing in real estate",vol:150,pos:null,traffic:45,kd:null,intent:"Informational",page:"Blog"},
    {kw:"fast roi",vol:90,pos:null,traffic:39,kd:null,intent:"Commercial",page:"Blog"},
    {kw:"ground floor investing",vol:70,pos:1,traffic:25,kd:3,intent:"Branded",page:"Homepage"},
    {kw:"ground floor login",vol:70,pos:2,traffic:19,kd:6,intent:"Branded",page:"Homepage"}
];

const GAP_DATA = [
    {kw:"Real estate investing for beginners",vol:5200,kd:35,est:"500-1,500"},
    {kw:"Real estate crowdfunding platforms",vol:1800,kd:72,est:"300-800"},
    {kw:"Crowdfunding real estate",vol:1100,kd:76,est:"100-300"},
    {kw:"Fractional real estate investing",vol:800,kd:21,est:"200-400"},
    {kw:"Passive real estate investing",vol:600,kd:28,est:"150-300"},
    {kw:"What is real estate crowdfunding",vol:500,kd:1,est:"200-500"},
    {kw:"Invest in real estate online",vol:800,kd:82,est:"100-250"},
    {kw:"Best RE crowdfunding sites",vol:200,kd:49,est:"50-150"},
    {kw:"RE crowdfunding returns",vol:200,kd:7,est:"80-150"}
];

// ========== CHART COLORS ==========
const BLUE = '#1565C0';
const BLUE_LIGHT = 'rgba(21,101,192,0.15)';
const RED = '#C62828';
const RED_LIGHT = 'rgba(198,40,40,0.15)';
const GREEN = '#2E7D32';
const GREEN_LIGHT = 'rgba(46,125,50,0.15)';
const ORANGE = '#E65100';
const GRAY = '#9E9E9E';

Chart.defaults.font.family = "-apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif";
Chart.defaults.font.size = 12;
Chart.defaults.color = '#616161';

// ========== TAB NAVIGATION ==========
document.querySelectorAll('.nav-tab').forEach(tab => {
    tab.addEventListener('click', () => {
        document.querySelectorAll('.nav-tab').forEach(t => t.classList.remove('active'));
        document.querySelectorAll('.section').forEach(s => s.classList.remove('active'));
        tab.classList.add('active');
        document.getElementById(tab.dataset.tab).classList.add('active');
    });
});

// ========== SCORE RINGS ==========
function drawRing(id, score, color) {
    const ctx = document.getElementById(id).getContext('2d');
    new Chart(ctx, {
        type: 'doughnut',
        data: {
            datasets: [{
                data: [score, 100 - score],
                backgroundColor: [color, '#EEEEEE'],
                borderWidth: 0
            }]
        },
        options: {
            cutout: '78%',
            responsive: false,
            plugins: { legend: { display: false }, tooltip: { enabled: false } },
            animation: { animateRotate: true, duration: 1200 }
        }
    });
}
drawRing('scoreGF', 20, RED);
drawRing('scoreFR', 74, GREEN);

// ========== TRAFFIC TREND ==========
new Chart(document.getElementById('trafficTrend'), {
    type: 'line',
    data: {
        labels: MONTHS_12,
        datasets: [{
            label: 'Groundfloor',
            data: GF_TRAFFIC,
            borderColor: BLUE,
            backgroundColor: BLUE_LIGHT,
            fill: true,
            tension: 0.3,
            pointRadius: 4,
            pointBackgroundColor: BLUE
        }]
    },
    options: {
        responsive: true,
        plugins: {
            legend: { display: false },
            tooltip: { callbacks: { label: ctx => ctx.parsed.y.toLocaleString() + ' visits' } }
        },
        scales: {
            y: { beginAtZero: false, ticks: { callback: v => (v/1000).toFixed(0)+'K' }, grid: { color: '#F0F0F0' } },
            x: { grid: { display: false } }
        }
    }
});

// ========== REFDOMAINS TREND ==========
new Chart(document.getElementById('refdomainsTrend'), {
    type: 'line',
    data: {
        labels: MONTHS_6,
        datasets: [{
            label: 'Groundfloor',
            data: GF_REFDOMAINS,
            borderColor: GREEN,
            backgroundColor: GREEN_LIGHT,
            fill: true,
            tension: 0.3,
            pointRadius: 4,
            pointBackgroundColor: GREEN
        }]
    },
    options: {
        responsive: true,
        plugins: {
            legend: { display: false },
            tooltip: { callbacks: { label: ctx => ctx.parsed.y.toLocaleString() + ' domains' } }
        },
        scales: {
            y: { beginAtZero: false, grid: { color: '#F0F0F0' } },
            x: { grid: { display: false } }
        }
    }
});

// ========== SCORE BREAKDOWN ==========
new Chart(document.getElementById('scoreBreakdown'), {
    type: 'bar',
    data: {
        labels: ['Organic Traffic','Keywords','Top 3 %','Domain Rating','Traffic Trend','Traffic Value'],
        datasets: [
            { label: 'Groundfloor', data: [15,28,16,49,25,5], backgroundColor: BLUE },
            { label: 'Fundrise', data: [100,100,25,73,30,100], backgroundColor: GRAY }
        ]
    },
    options: {
        responsive: true,
        indexAxis: 'y',
        plugins: { legend: { position: 'bottom' } },
        scales: {
            x: { max: 100, grid: { color: '#F0F0F0' }, ticks: { callback: v => v + '/100' } },
            y: { grid: { display: false } }
        }
    }
});

// ========== TRAFFIC COMPOSITION ==========
new Chart(document.getElementById('trafficComposition'), {
    type: 'doughnut',
    data: {
        labels: ['Branded Traffic (88%)','Non-Branded Traffic (12%)'],
        datasets: [{
            data: [88, 12],
            backgroundColor: [BLUE, ORANGE],
            borderWidth: 2,
            borderColor: '#fff'
        }]
    },
    options: {
        responsive: true,
        cutout: '55%',
        plugins: {
            legend: { position: 'bottom' },
            tooltip: { callbacks: { label: ctx => ctx.label + ': ~' + (ctx.parsed === 88 ? '7,200' : '1,000') + ' visits/mo' } }
        }
    }
});

// ========== KEYWORD POSITION DISTRIBUTION ==========
new Chart(document.getElementById('kwPositions'), {
    type: 'bar',
    data: {
        labels: ['Top 3','4-10','11-50','51-100'],
        datasets: [
            { label: 'Groundfloor', data: [107,207,263,100], backgroundColor: BLUE },
            { label: 'Fundrise', data: [608,843,694,300], backgroundColor: GRAY }
        ]
    },
    options: {
        responsive: true,
        plugins: { legend: { position: 'bottom' } },
        scales: {
            y: { grid: { color: '#F0F0F0' } },
            x: { grid: { display: false } }
        }
    }
});

// ========== TOP KEYWORDS BY TRAFFIC ==========
const topKW = KEYWORDS.filter(k => !k.kw.includes('groundfloor') && !k.kw.includes('ground floor') && !k.kw.includes('grounfloor')).sort((a,b) => b.traffic - a.traffic).slice(0,8);
new Chart(document.getElementById('kwTraffic'), {
    type: 'bar',
    data: {
        labels: topKW.map(k => k.kw.length > 30 ? k.kw.slice(0,28)+'...' : k.kw),
        datasets: [{
            label: 'Monthly Traffic',
            data: topKW.map(k => k.traffic),
            backgroundColor: topKW.map(k => k.pos <= 3 ? GREEN : k.pos <= 10 ? BLUE : ORANGE)
        }]
    },
    options: {
        responsive: true,
        indexAxis: 'y',
        plugins: { legend: { display: false } },
        scales: {
            x: { grid: { color: '#F0F0F0' } },
            y: { grid: { display: false }, ticks: { font: { size: 11 } } }
        }
    }
});

// ========== KEYWORD TABLE ==========
const kwTbody = document.querySelector('#kwTable tbody');
KEYWORDS.forEach(k => {
    const isBranded = k.intent === 'Branded';
    const tr = document.createElement('tr');
    tr.innerHTML = `
        <td>${k.kw}</td>
        <td>${k.vol ? k.vol.toLocaleString() : '-'}</td>
        <td>${k.pos || '-'}</td>
        <td>${k.traffic.toLocaleString()}</td>
        <td>${k.kd !== null ? k.kd : '-'}</td>
        <td><span class="badge ${isBranded ? 'badge-blue' : k.intent === 'Commercial' ? 'badge-orange' : 'badge-green'}">${k.intent}</span></td>
        <td style="font-size:12px;color:var(--gray-600);max-width:200px;overflow:hidden;text-overflow:ellipsis">${k.page}</td>
    `;
    kwTbody.appendChild(tr);
});

// ========== COMPETITOR TRAFFIC COMPARISON ==========
new Chart(document.getElementById('compTraffic'), {
    type: 'line',
    data: {
        labels: MONTHS_12,
        datasets: [
            { label: 'Groundfloor', data: GF_TRAFFIC, borderColor: BLUE, backgroundColor: BLUE_LIGHT, fill: true, tension: 0.3, pointRadius: 3 },
            { label: 'Fundrise', data: FR_TRAFFIC, borderColor: RED, backgroundColor: RED_LIGHT, fill: true, tension: 0.3, pointRadius: 3 }
        ]
    },
    options: {
        responsive: true,
        plugins: {
            legend: { position: 'bottom' },
            tooltip: { callbacks: { label: ctx => ctx.dataset.label + ': ' + ctx.parsed.y.toLocaleString() } }
        },
        scales: {
            y: { ticks: { callback: v => (v/1000).toFixed(0)+'K' }, grid: { color: '#F0F0F0' } },
            x: { grid: { display: false } }
        }
    }
});

// ========== KEYWORD COVERAGE COMPARISON ==========
new Chart(document.getElementById('compKeywords'), {
    type: 'bar',
    data: {
        labels: ['Total Keywords','Top 3','Top 4-10','Top 11+'],
        datasets: [
            { label: 'Groundfloor', data: [677,107,207,455], backgroundColor: BLUE },
            { label: 'Fundrise', data: [2445,608,843,1343], backgroundColor: RED }
        ]
    },
    options: {
        responsive: true,
        plugins: { legend: { position: 'bottom' } },
        scales: {
            y: { ticks: { callback: v => v.toLocaleString() }, grid: { color: '#F0F0F0' } },
            x: { grid: { display: false } }
        }
    }
});

// ========== CONTENT GAP BUBBLE ==========
new Chart(document.getElementById('gapBubble'), {
    type: 'bubble',
    data: {
        datasets: GAP_DATA.map((g, i) => ({
            label: g.kw,
            data: [{ x: g.kd, y: g.vol, r: Math.max(6, Math.sqrt(g.vol) / 2) }],
            backgroundColor: g.kd < 30 ? 'rgba(46,125,50,0.6)' : g.kd < 60 ? 'rgba(230,81,0,0.6)' : 'rgba(198,40,40,0.6)',
            borderColor: g.kd < 30 ? GREEN : g.kd < 60 ? ORANGE : RED,
            borderWidth: 1
        }))
    },
    options: {
        responsive: true,
        plugins: {
            legend: { display: false },
            tooltip: {
                callbacks: {
                    label: ctx => {
                        const d = GAP_DATA[ctx.datasetIndex];
                        return [d.kw, 'Volume: ' + d.vol.toLocaleString(), 'KD: ' + d.kd, 'Est. traffic: ' + d.est];
                    }
                }
            }
        },
        scales: {
            x: { title: { display: true, text: 'Keyword Difficulty', font: { weight: 'bold' } }, min: 0, max: 100, grid: { color: '#F0F0F0' } },
            y: { title: { display: true, text: 'Monthly Search Volume', font: { weight: 'bold' } }, ticks: { callback: v => v.toLocaleString() }, grid: { color: '#F0F0F0' } }
        }
    }
});

// ========== REFERRING DOMAINS DR ==========
const refDomains = [
    {d:'google.com',dr:99,links:2},{d:'youtube.com',dr:99,links:41},{d:'apple.com',dr:97,links:59},
    {d:'wikipedia.org',dr:97,links:2},{d:'github.com',dr:96,links:2},{d:'squarespace.com',dr:95,links:134},
    {d:'medium.com',dr:94,links:3},{d:'yahoo.com',dr:94,links:12},{d:'substack.com',dr:93,links:3},
    {d:'bbb.org',dr:93,links:1},{d:'businessinsider.com',dr:92,links:3},{d:'bloomberg.com',dr:92,links:2},
    {d:'investopedia.com',dr:92,links:18}
];
new Chart(document.getElementById('refDomainsDR'), {
    type: 'bar',
    data: {
        labels: refDomains.map(r => r.d),
        datasets: [{
            label: 'Domain Rating',
            data: refDomains.map(r => r.dr),
            backgroundColor: refDomains.map(r => r.dr >= 95 ? GREEN : BLUE)
        }]
    },
    options: {
        responsive: true,
        indexAxis: 'y',
        plugins: {
            legend: { display: false },
            tooltip: { callbacks: { afterLabel: ctx => refDomains[ctx.dataIndex].links + ' backlinks' } }
        },
        scales: {
            x: { min: 88, max: 100, grid: { color: '#F0F0F0' } },
            y: { grid: { display: false }, ticks: { font: { size: 11 } } }
        }
    }
});

// ========== REFDOMAINS GROWTH COMPARISON ==========
new Chart(document.getElementById('refDomainsGrowth'), {
    type: 'line',
    data: {
        labels: MONTHS_6,
        datasets: [
            { label: 'Groundfloor', data: GF_REFDOMAINS, borderColor: GREEN, backgroundColor: GREEN_LIGHT, fill: true, tension: 0.3, pointRadius: 4, yAxisID: 'y' },
            { label: 'Fundrise', data: FR_REFDOMAINS, borderColor: RED, backgroundColor: RED_LIGHT, fill: true, tension: 0.3, pointRadius: 4, yAxisID: 'y1' }
        ]
    },
    options: {
        responsive: true,
        plugins: { legend: { position: 'bottom' } },
        scales: {
            y: { type: 'linear', position: 'left', title: { display: true, text: 'Groundfloor' }, grid: { color: '#F0F0F0' } },
            y1: { type: 'linear', position: 'right', title: { display: true, text: 'Fundrise' }, grid: { drawOnChartArea: false } },
            x: { grid: { display: false } }
        }
    }
});

// ========== TABLE SORTING ==========
function sortTable(tableId, colIndex) {
    const table = document.getElementById(tableId);
    const tbody = table.querySelector('tbody');
    const rows = Array.from(tbody.querySelectorAll('tr'));
    const th = table.querySelectorAll('thead th')[colIndex];
    const asc = !th.classList.contains('sorted') || th.dataset.dir === 'desc';

    table.querySelectorAll('thead th').forEach(h => { h.classList.remove('sorted'); h.dataset.dir = ''; });
    th.classList.add('sorted');
    th.dataset.dir = asc ? 'asc' : 'desc';
    th.querySelector('.sort-arrow').textContent = asc ? '\u25B2' : '\u25BC';

    rows.sort((a, b) => {
        let va = a.cells[colIndex].textContent.replace(/[,$%]/g,'').trim();
        let vb = b.cells[colIndex].textContent.replace(/[,$%]/g,'').trim();
        const na = parseFloat(va), nb = parseFloat(vb);
        if (!isNaN(na) && !isNaN(nb)) return asc ? na - nb : nb - na;
        return asc ? va.localeCompare(vb) : vb.localeCompare(va);
    });
    rows.forEach(r => tbody.appendChild(r));
}
</script>
</body>
</html>
