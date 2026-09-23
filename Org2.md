Subject: For discussion: Aligning our organizational structure to our objectives

Team,

As we stand up the new organization, one of the first decisions in front of us is how we structure ourselves. I'd like to put an option on the table and share the reasoning and evidence behind it. My goal is to make sure our structure gives us the best possible chance of meeting the objectives we've been given: consolidating systems, improving the user experience, being agile and responsive to mission needs, and delivering quickly. I've attached two figures for reference and would welcome challenges, alternatives, and anything I've missed.

STARTING POINT

Our familiar model of offices, groups, divisions, and branches has served the institution for a long time. It provides clear accountability, well-understood supervisory chains, and stable ownership of systems. Those are real strengths, and any alternative should preserve them. The question is whether that model is the best fit for the specific objectives we've been set. The research on software organizations suggests there are tradeoffs worth considering.

HOW STRUCTURE AFFECTS SOFTWARE DELIVERY

1. Structure shapes architecture. Conway's Law observes that systems tend to mirror the communication structures of the organizations that build them, and research on real codebases (MacCormack, Rusnak, and Baldwin, 2012) supports it. In practice, organizational boundaries tend to become system boundaries. If our goal is a consolidated, composable architecture, it helps to have an organization shaped the same way.

2. Where decisions are made. Software development involves a high degree of uncertainty, and the information needed to make good decisions often sits with the teams closest to users and code. This parallels the principle behind mission command: leadership sets intent, and execution decisions are made at the edge.

3. Handoffs and coordination. Each organizational layer adds coordination points, and much of software lead time is spent waiting on handoffs and approvals. The DORA research (Forsgren, Humble, and Kim, Accelerate, 2018) finds that teams able to deliver without extensive cross-team coordination tend to perform better.

4. Information flow. In deeper hierarchies, intent and status pass through more translation points, which can slow and blur the picture in both directions.

5. Incentives. When budgets, metrics, and ownership are aligned to branches, it is natural and rational for leaders to optimize for their area. This is a property of the structure, not of the people in it.

6. Adaptability. When team boundaries follow the chain of command, adjusting them to fit an evolving architecture requires formal reorganization, which is slow and disruptive.

HOW THIS RELATES TO OUR OBJECTIVES

The traditional model is optimized for stable ownership of discrete systems. Each of our objectives involves working across those boundaries.

System consolidation: When each system is owned by a branch, consolidation can mean asking a team to retire its own portfolio, which creates understandable friction. Separate branches also tend to produce separate systems over time, which is part of how overlap accumulates.

User experience: Users experience workflows that span many systems. When ownership is divided by branch, no one is positioned to own the end-to-end journey, and organizational seams can show up as inconsistencies in the interface.

Agility and responsiveness: When people and funding are tied to branches, shifting effort toward emerging priorities requires coordination across several chains of command.

Delivering quickly: When a single capability spans multiple branches and divisions, delivery pace is set by the slowest dependency, and coordination costs grow with each boundary a change crosses.

WHAT THE EVIDENCE SAYS

The DORA research program, the largest longitudinal study of software delivery performance, consistently finds that team autonomy and loosely coupled architecture are associated with higher delivery performance. Puppet's State of DevOps research found that organizations with clearly defined team responsibilities tend to be more mature, and recommends stream-aligned and platform teams as described in Team Topologies. Amazon found that the strongest predictor of team success was not team size but a dedicated leader with the authority and experience to run a team with a single focus, and it gauges autonomy by whether a team can release its changes without coordination and approvals from other teams. Within DoD, the Defense Innovation Board's 2019 study, "Software Is Never Done," concluded that the Department's software approach was too slow and too costly and delayed warfighter access to needed tools. Kessel Run offers a useful case: its leadership described moving from years of investment without fielded software to delivering capability thousands of times a year, with product teams organized around identifying and solving mission problems.

APPLICABILITY TO OUR ENVIRONMENT

A fair question is whether examples like Amazon apply to an institution with our level of oversight, process, and mix of government and contractor staff. Kessel Run is a closer comparison. It is a government program office operating in the same acquisition system, and a 2022 RAND report counted 1,179 personnel, of whom 863 were contractors. It is also still formally organized into branches and serves as a program office for multiple programs of record. The formal structure meets institutional requirements, while the work itself is organized around product teams. That is the balance this proposal aims for.

Our process requirements can also be addressed through this model. Rather than each layer of the hierarchy adding its own reviews, required process such as security, compliance, ATO, and architecture standards can be built into the shared platforms and pipelines every team uses, so compliance happens by default. We keep the rigor while reducing wait time.

On managing people: every government employee would still have a clear supervisor of record through their practice, with defined spans of control, performance management, and career paths. For contractors, contracts and task orders can be aligned to mission streams and platforms with clear outcomes. A government product owner and COR within each stream would set priorities through the backlog, while contractor leads continue to manage their own staff, preserving the boundary against personal services.

FTE CONSIDERATIONS

We are standing up this office under tight FTE constraints and high expectations for mission agility, which puts a premium on how we use each position. Every management layer requires leadership billets. As a notional example, an office with three groups, three divisions per group, and three branches per division would need about 40 leadership positions before deputies, roughly 20 percent of a 200-person organization. FTE allocations are also long-lived. Once a position is assigned to a requirement, it is typically committed for two to five years, depending on how long the incumbent stays before rotating. A flatter structure keeps the leadership core small and places more of our FTEs directly on delivery. Because teams are persistent and aligned to outcomes, capacity can be redirected through regular planning rather than waiting for positions to turn over.

THE TEAM TOPOLOGIES MODEL (Figure 1)

Team Topologies (Skelton and Pais, 2019) organizes teams around the flow of work to users and is designed to keep any one team's scope manageable. It defines four team types:

- Stream-aligned teams own a mission outcome or user journey end to end. Most teams are this type.
- Platform teams provide self-service capabilities that stream teams can consume without negotiation.
- Enabling teams help stream teams build new capabilities, then step back.
- Complicated-subsystem teams own areas that require deep specialist knowledge.

It also defines three interaction modes so that dependencies between teams are designed up front: collaboration (close, time-boxed work to explore something new), X-as-a-service (consuming another team's capability with minimal coordination), and facilitating (one team helping another build capability).

WHAT THIS COULD LOOK LIKE FOR US (Figure 2)

- Office leadership stays small and owns commander's intent, portfolio, budget, and governance.
- Mission streams take the place of groups and divisions, each with three to five stream-aligned teams and a product, engineering, and UX lead.
- A platform group runs our capability platforms and AI orchestration layer as internal products.
- Enabling and complicated-subsystem teams support the streams where needed.
- Practices (engineering, UX, QA, data) serve as the home for people. Practice leads are supervisors of record for performance, hiring, and career growth, while day-to-day priorities come from the team.

RISKS AND OPEN QUESTIONS

This model has real risks, and I want to be upfront about them:

- Transition is hard. Research on Team Topologies adoption finds the move away from traditional structures is where organizations struggle most.
- Dual lines of direction can create ambiguity. We would need clearly documented decision rights between practice leads and stream leadership.
- Platforms can become new bottlenecks if they aren't run as products, and their benefits tend to erode without ongoing investment.
- Models adopted in name only tend to underdeliver. Spotify's widely copied structure is a cautionary example.
- Position classification and formal org chart requirements will need early engagement with HR.

These are the reasons I'd like us to work through this together rather than treat it as settled.

WHY NOW

Because we are already making structural decisions as part of the convergence, this is the point where changing course costs the least. Adjusting later would likely mean a second round of disruption for our people. There's a saying I've always found useful: "If you always do what you've always done, you'll always be where you've always been." Standing up a new organization gives us a rare opportunity to be intentional about how we're structured, and I think it's worth taking the time to get it right.

I'd like to set aside time at our next leadership sync to walk through this, and I'm happy to meet one-on-one beforehand with anyone who'd like to talk it through.

Build well,
Adam
