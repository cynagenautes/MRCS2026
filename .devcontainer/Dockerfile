# syntax=docker/dockerfile:1
FROM texlive/texlive:latest

# ミラーをICSCoEに変更
RUN sed -i.bak -E '/^URIs:/ {N; /Suites:.*-security/! {s@http://deb\.debian\.org/debian/?@https://ftp.udx.icscoe.jp/Linux/debian/@;}}' /etc/apt/sources.list.d/debian.sources
