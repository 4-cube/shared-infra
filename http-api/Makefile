.PHONY: validate deploy destroy debug

REGION := $(or ${AWS_REGION},"eu-west-1")

validate:
	sam validate

deploy:
	sam deploy --stack-name http-api --capabilities CAPABILITY_IAM --region ${REGION} --no-confirm-changeset

destroy:
	aws cloudformation delete-stack --stack-name http-api --region ${REGION}

debug:
	@echo ${REGION}
