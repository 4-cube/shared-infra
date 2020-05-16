.PHONY: validate deploy destroy debug

REGION := $(or ${AWS_REGION},"eu-west-1")
STACK_NAME := "http-apigw"

validate:
	sam validate

deploy:
	sam deploy --stack-name ${STACK_NAME} --capabilities CAPABILITY_IAM --region ${REGION} --no-confirm-changeset

destroy:
	aws cloudformation delete-stack --stack-name ${STACK_NAME} --region ${REGION}

debug:
	@echo ${REGION}
	@echo ${STACK_NAME}
