FROM alpine:3.18 as builder

RUN apk add --no-cache git
RUN git clone -b redmine4.2  https://github.com/farend/redmine_theme_farend_bleuclair.git

FROM redmine:5.1.1-alpine3.18 as runner

COPY --from=builder /redmine_theme_farend_bleuclair public/themes/bleuclair
