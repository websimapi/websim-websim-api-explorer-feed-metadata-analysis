# WebSim API Metadata & Feed Analysis

This document provides a comprehensive analysis of WebSim's API capabilities, particularly focusing on the distinction between "hot" page contents and general "trending" feeds, along with detailed metadata extraction possibilities.

## Key Finding: Hot vs Trending - They're Actually the Same Endpoint!

**Important Discovery**: The WebSim API does NOT have separate "hot" and "trending" endpoints. Instead, it has a single `/api/v1/feed/trending` endpoint that accepts a `feed` parameter to specify different ranking algorithms, including "hot".

### Feed Algorithm Types Available

The API offers multiple sophisticated ranking algorithms:

#### Core Algorithms
- **`hot`** (default): Combines recent popularity with engagement velocity
- **`new`**: Chronological ordering by creation date
- **`top`**: Ranked by total cumulative engagement
- **`engaging`**: High engagement rate prioritization
- **`viral`**: Exponential growth pattern detection

#### Platform-Specific Variants
- **`engaging_mobile`**: Mobile-optimized engagement algorithm
- **`hot_desktop`**: Desktop-optimized hot content
- **`hot_mobile`**: Mobile-optimized hot content  
- **`hot_mobile_unplayed`**: Mobile hot content for new users
- **`featured_desktop`**: Curated desktop content
- **`featured_mobile`**: Curated mobile content

#### Behavioral Algorithms
- **`recommended`**: Personalized recommendations
- **`following`**: Content from followed users
- **`recently_played`**: User's recent activity
- **`most_replayed`**: High replay value content
- **`most_replayed_mobile`**: Mobile replay-optimized

#### Special Categories
- **`multiplayer_active_sessions`**: Live multiplayer content

## Metadata Extraction Capabilities

### 1. Project-Level Metadata

