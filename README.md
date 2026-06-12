# Forecast Feature Backfilling

A project page about rebuilding historical forecast features so a hybrid time-series and supervised model can train correctly.

## Project Website

[View Project Site](https://mah-trigui.github.io/forecast-feature-backfilling/)

## Overview

This project forecasts weekly sea turtle rescue counts across 29 sites using a hybrid architecture:
- a per-site time-series forecast baseline
- a supervised correction model

The key issue was that the forecast could not be used as a feature unless it also existed historically in the training rows.

## Core Idea

The forecast feature was rebuilt historically using expanding-window forecasts for earlier years, so the supervised model could train on rows where both were available:
- forecast baseline
- actual outcome

## Architecture

![Architecture](images/architecture.jpg)

## Key Takeaway

**A forecast feature is only valid after its history has been recreated.**

## Public Scope

This repository shares the architecture idea, selected implementation logic, and project presentation only.
