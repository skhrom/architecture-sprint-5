2025-02-18 17:49:07 DEBUG    rasa.core.processor  - [debug    ] processor.message.parse        parse_data_entities=[] parse_data_intent={'name': 'ask_architecture', 'confidence': 0.27118220925331116} parse_data_text=Привет
2025-02-18 17:49:07 DEBUG    rasa.core.processor  - Logged UserUtterance - tracker now has 4 events.
2025-02-18 17:49:07 DEBUG    rasa.core.actions.action  - Validating extracted slots: topic
2025-02-18 17:49:07 DEBUG    rasa.core.processor  - [debug    ] processor.extract.slots        action_extract_slot=action_extract_slots len_extraction_events=1 rasa_events=[SlotSet(key: topic, value: Привет)]
2025-02-18 17:49:07 DEBUG    rasa.engine.runner.dask  - Running graph with inputs: {'__tracker__': <rasa.shared.core.trackers.DialogueStateTracker object at 0x0000024F273C79D0>}, targets: ['select_prediction'] and ExecutionContext(model_id='1e2ff5c0db8a4015ad3ee3d512ae0e80', should_add_diagnostic_data=False, is_finetuning=False, node_name=None).
2025-02-18 17:49:07 DEBUG    rasa.engine.graph  - Node 'rule_only_data_provider' running 'RuleOnlyDataProvider.provide'.
2025-02-18 17:49:07 DEBUG    rasa.engine.graph  - Node 'domain_provider' running 'DomainProvider.provide_inference'.
2025-02-18 17:49:07 DEBUG    rasa.engine.graph  - Node 'run_MemoizationPolicy0' running 'MemoizationPolicy.predict_action_probabilities'.
2025-02-18 17:49:07 DEBUG    rasa.core.policies.memoization  - [debug    ] memoization.predict.actions    tracker_states=[{}, {'user': {'intent': 'ask_architecture'}, 'prev_action': {'action_name': 'action_listen'}}]
2025-02-18 17:49:07 DEBUG    rasa.core.policies.memoization  - There is no memorised next action
2025-02-18 17:49:07 DEBUG    rasa.engine.graph  - Node 'run_RulePolicy1' running 'RulePolicy.predict_action_probabilities'.
2025-02-18 17:49:07 DEBUG    rasa.core.policies.rule_policy  - [debug    ] rule_policy.actions.find       current_states=
[state 1] user text: Привет | previous action name: action_listen
2025-02-18 17:49:07 DEBUG    rasa.core.policies.rule_policy  - There is no applicable rule.
2025-02-18 17:49:07 DEBUG    rasa.core.policies.rule_policy  - [debug    ] rule_policy.actions.find       current_states=
[state 1] user intent: ask_architecture | previous action name: action_listen
2025-02-18 17:49:07 DEBUG    rasa.core.policies.rule_policy  - There is a rule for the next action 'utter_architecture_response'.
2025-02-18 17:49:07 DEBUG    rasa.engine.graph  - Node 'run_TEDPolicy2' running 'TEDPolicy.predict_action_probabilities'.
2025-02-18 17:49:07 DEBUG    rasa.core.policies.ted_policy  - TED predicted 'action_deactivate_loop' based on user intent.
2025-02-18 17:49:07 DEBUG    rasa.engine.graph  - Node 'select_prediction' running 'DefaultPolicyPredictionEnsemble.combine_predictions_from_kwargs'.
2025-02-18 17:49:07 DEBUG    rasa.core.policies.ensemble  - Made prediction using user intent.
2025-02-18 17:49:07 DEBUG    rasa.core.policies.ensemble  - Added `DefinePrevUserUtteredFeaturization(False)` event.
2025-02-18 17:49:07 DEBUG    rasa.core.policies.ensemble  - Predicted next action using RulePolicy.
2025-02-18 17:49:07 DEBUG    rasa.core.processor  - Predicted next action 'utter_architecture_response' with confidence 1.00.
2025-02-18 17:49:07 DEBUG    rasa.core.processor  - [debug    ] processor.actions.policy_prediction prediction_events=[<rasa.shared.core.events.DefinePrevUserUtteredFeaturization object at 0x0000024F2B48BA00>]
2025-02-18 17:49:07 DEBUG    rasa.core.processor  - [debug    ] processor.actions.log          action_name=utter_architecture_response rasa_events=[BotUttered('Архитектура ПО включает выбор структур, которые обеспечивают масштабируемость, гибкость и поддерживаемость приложения. Задайте конкретный вопрос по этой теме, и я помогу вам с информацией.', {"elements": null, "quick_replies": null, "buttons": null, "attachment": null, "image": null, "custom": null}, {"utter_action": "utter_architecture_response"}, 1739890147.4251552)]
2025-02-18 17:49:07 DEBUG    rasa.engine.runner.dask  - Running graph with inputs: {'__tracker__': <rasa.shared.core.trackers.DialogueStateTracker object at 0x0000024F273C79D0>}, targets: ['select_prediction'] and ExecutionContext(model_id='1e2ff5c0db8a4015ad3ee3d512ae0e80', should_add_diagnostic_data=False, is_finetuning=False, node_name=None).
2025-02-18 17:49:07 DEBUG    rasa.engine.graph  - Node 'rule_only_data_provider' running 'RuleOnlyDataProvider.provide'.
2025-02-18 17:49:07 DEBUG    rasa.engine.graph  - Node 'domain_provider' running 'DomainProvider.provide_inference'.
2025-02-18 17:49:07 DEBUG    rasa.engine.graph  - Node 'run_MemoizationPolicy0' running 'MemoizationPolicy.predict_action_probabilities'.
2025-02-18 17:49:07 DEBUG    rasa.core.policies.memoization  - [debug    ] memoization.predict.actions    tracker_states=[{'user': {'intent': 'ask_architecture'}, 'prev_action': {'action_name': 'action_listen'}}, {'user': {'intent': 'ask_architecture'}, 'prev_action': {'action_name': 'utter_architecture_response'}}]
2025-02-18 17:49:07 DEBUG    rasa.core.policies.memoization  - There is a memorised next action 'action_listen'
2025-02-18 17:49:07 DEBUG    rasa.engine.graph  - Node 'run_RulePolicy1' running 'RulePolicy.predict_action_probabilities'.
2025-02-18 17:49:07 DEBUG    rasa.core.policies.rule_policy  - [debug    ] rule_policy.actions.find       current_states=
[state 1] user intent: ask_architecture | previous action name: action_listen
[state 2] user intent: ask_architecture | previous action name: utter_architecture_response
2025-02-18 17:49:07 DEBUG    rasa.core.policies.rule_policy  - There is a rule for the next action 'action_listen'.
2025-02-18 17:49:07 DEBUG    rasa.engine.graph  - Node 'run_TEDPolicy2' running 'TEDPolicy.predict_action_probabilities'.
2025-02-18 17:49:07 DEBUG    rasa.core.policies.ted_policy  - TED predicted 'action_listen' based on user intent.
2025-02-18 17:49:07 DEBUG    rasa.engine.graph  - Node 'select_prediction' running 'DefaultPolicyPredictionEnsemble.combine_predictions_from_kwargs'.
2025-02-18 17:49:07 DEBUG    rasa.core.policies.ensemble  - Predicted next action using RulePolicy.
2025-02-18 17:49:07 DEBUG    rasa.core.processor  - Predicted next action 'action_listen' with confidence 1.00.
2025-02-18 17:49:07 DEBUG    rasa.core.processor  - [debug    ] processor.actions.policy_prediction prediction_events=[]
2025-02-18 17:49:07 DEBUG    rasa.core.processor  - [debug    ] processor.actions.log          action_name=action_listen rasa_events=[]
2025-02-18 17:49:07 DEBUG    rasa.core.tracker_store  - No event broker configured. Skipping streaming events.
2025-02-18 17:49:07 DEBUG    rasa.core.lock_store  - Deleted lock for conversation 'PractikumStudent'.
2025-02-18 17:49:18 DEBUG    rasa.core.lock_store  - Issuing ticket for conversation 'PractikumStudent'.
2025-02-18 17:49:18 DEBUG    rasa.core.lock_store  - Acquiring lock for conversation 'PractikumStudent'.
2025-02-18 17:49:18 DEBUG    rasa.core.lock_store  - Acquired lock for conversation 'PractikumStudent'.
2025-02-18 17:49:18 DEBUG    rasa.core.tracker_store  - Recreating tracker for id 'PractikumStudent'
2025-02-18 17:49:18 DEBUG    rasa.engine.runner.dask  - Running graph with inputs: {'__message__': [<rasa.core.channels.channel.UserMessage object at 0x0000024F25FD7610>], '__tracker__': <rasa.shared.core.trackers.DialogueStateTracker object at 0x0000024F2B4DD360>}, targets: ['run_RegexMessageHandler'] and ExecutionContext(model_id='1e2ff5c0db8a4015ad3ee3d512ae0e80', should_add_diagnostic_data=False, is_finetuning=False, node_name=None).
2025-02-18 17:49:18 DEBUG    rasa.engine.graph  - Node 'nlu_message_converter' running 'NLUMessageConverter.convert_user_message'.
2025-02-18 17:49:18 DEBUG    rasa.engine.graph  - Node 'run_WhitespaceTokenizer0' running 'WhitespaceTokenizer.process'.
2025-02-18 17:49:18 DEBUG    rasa.engine.graph  - Node 'run_RegexFeaturizer1' running 'RegexFeaturizer.process'.
2025-02-18 17:49:18 DEBUG    rasa.engine.graph  - Node 'run_LexicalSyntacticFeaturizer2' running 'LexicalSyntacticFeaturizer.process'.
2025-02-18 17:49:18 DEBUG    rasa.engine.graph  - Node 'run_CountVectorsFeaturizer3' running 'CountVectorsFeaturizer.process'.
2025-02-18 17:49:18 DEBUG    rasa.engine.graph  - Node 'run_LanguageModelFeaturizer4' running 'LanguageModelFeaturizer.process'.
2025-02-18 17:49:18 DEBUG    rasa.engine.graph  - Node 'run_DIETClassifier5' running 'DIETClassifier.process'.
2025-02-18 17:49:18 DEBUG    rasa.engine.graph  - Node 'run_EntitySynonymMapper6' running 'EntitySynonymMapper.process'.
2025-02-18 17:49:18 DEBUG    rasa.engine.graph  - Node 'run_ResponseSelector7' running 'ResponseSelector.process'.
2025-02-18 17:49:18 DEBUG    rasa.nlu.classifiers.diet_classifier  - There is no trained model for 'ResponseSelector': The component is either not trained or didn't receive enough training data.
2025-02-18 17:49:18 DEBUG    rasa.nlu.selectors.response_selector  - Adding following selector key to message property: default
2025-02-18 17:49:18 DEBUG    rasa.engine.graph  - Node 'domain_provider' running 'DomainProvider.provide_inference'.
2025-02-18 17:49:18 DEBUG    rasa.engine.graph  - Node 'run_RegexMessageHandler' running 'RegexMessageHandler.process'.
2025-02-18 17:49:18 DEBUG    rasa.core.processor  - [debug    ] processor.message.parse        parse_data_entities=[] parse_data_intent={'name': 'ask_architecture', 'confidence': 0.27118220925331116} parse_data_text=Привет!
2025-02-18 17:49:18 DEBUG    rasa.core.processor  - Logged UserUtterance - tracker now has 10 events.
2025-02-18 17:49:18 DEBUG    rasa.core.actions.action  - Validating extracted slots: topic
2025-02-18 17:49:18 DEBUG    rasa.core.processor  - [debug    ] processor.extract.slots        action_extract_slot=action_extract_slots len_extraction_events=1 rasa_events=[SlotSet(key: topic, value: Привет!)]
2025-02-18 17:49:18 DEBUG    rasa.engine.runner.dask  - Running graph with inputs: {'__tracker__': <rasa.shared.core.trackers.DialogueStateTracker object at 0x0000024F2B4DD360>}, targets: ['select_prediction'] and ExecutionContext(model_id='1e2ff5c0db8a4015ad3ee3d512ae0e80', should_add_diagnostic_data=False, is_finetuning=False, node_name=None).
2025-02-18 17:49:18 DEBUG    rasa.engine.graph  - Node 'rule_only_data_provider' running 'RuleOnlyDataProvider.provide'.
2025-02-18 17:49:18 DEBUG    rasa.engine.graph  - Node 'domain_provider' running 'DomainProvider.provide_inference'.
2025-02-18 17:49:18 DEBUG    rasa.engine.graph  - Node 'run_MemoizationPolicy0' running 'MemoizationPolicy.predict_action_probabilities'.
2025-02-18 17:49:18 DEBUG    rasa.core.policies.memoization  - [debug    ] memoization.predict.actions    tracker_states=[{'user': {'intent': 'ask_architecture'}, 'prev_action': {'action_name': 'utter_architecture_response'}}, {'user': {'intent': 'ask_architecture'}, 'prev_action': {'action_name': 'action_listen'}}]
2025-02-18 17:49:18 DEBUG    rasa.core.policies.memoization  - There is no memorised next action
2025-02-18 17:49:18 DEBUG    rasa.engine.graph  - Node 'run_RulePolicy1' running 'RulePolicy.predict_action_probabilities'.
2025-02-18 17:49:18 DEBUG    rasa.core.policies.rule_policy  - [debug    ] rule_policy.actions.find       current_states=
[state 1] user intent: ask_architecture | previous action name: action_listen
[state 2] user intent: ask_architecture | previous action name: utter_architecture_response
[state 3] user text: Привет! | previous action name: action_listen
2025-02-18 17:49:18 DEBUG    rasa.core.policies.rule_policy  - There is no applicable rule.
2025-02-18 17:49:18 DEBUG    rasa.core.policies.rule_policy  - [debug    ] rule_policy.actions.find       current_states=
[state 1] user intent: ask_architecture | previous action name: action_listen
[state 2] user intent: ask_architecture | previous action name: utter_architecture_response
[state 3] user intent: ask_architecture | previous action name: action_listen
2025-02-18 17:49:18 DEBUG    rasa.core.policies.rule_policy  - There is a rule for the next action 'utter_architecture_response'.
2025-02-18 17:49:18 DEBUG    rasa.engine.graph  - Node 'run_TEDPolicy2' running 'TEDPolicy.predict_action_probabilities'.
2025-02-18 17:49:18 DEBUG    rasa.core.policies.ted_policy  - TED predicted 'action_deactivate_loop' based on user intent.
2025-02-18 17:49:18 DEBUG    rasa.engine.graph  - Node 'select_prediction' running 'DefaultPolicyPredictionEnsemble.combine_predictions_from_kwargs'.
2025-02-18 17:49:18 DEBUG    rasa.core.policies.ensemble  - Made prediction using user intent.
2025-02-18 17:49:18 DEBUG    rasa.core.policies.ensemble  - Added `DefinePrevUserUtteredFeaturization(False)` event.
2025-02-18 17:49:18 DEBUG    rasa.core.policies.ensemble  - Predicted next action using RulePolicy.
2025-02-18 17:49:18 DEBUG    rasa.core.processor  - Predicted next action 'utter_architecture_response' with confidence 1.00.
2025-02-18 17:49:18 DEBUG    rasa.core.processor  - [debug    ] processor.actions.policy_prediction prediction_events=[<rasa.shared.core.events.DefinePrevUserUtteredFeaturization object at 0x0000024F2B4895D0>]
2025-02-18 17:49:18 DEBUG    rasa.core.processor  - [debug    ] processor.actions.log          action_name=utter_architecture_response rasa_events=[BotUttered('Архитектура ПО включает выбор структур, которые обеспечивают масштабируемость, гибкость и поддерживаемость приложения. Задайте конкретный вопрос по этой теме, и я помогу вам с информацией.', {"elements": null, "quick_replies": null, "buttons": null, "attachment": null, "image": null, "custom": null}, {"utter_action": "utter_architecture_response"}, 1739890158.9392788)]
2025-02-18 17:49:18 DEBUG    rasa.engine.runner.dask  - Running graph with inputs: {'__tracker__': <rasa.shared.core.trackers.DialogueStateTracker object at 0x0000024F2B4DD360>}, targets: ['select_prediction'] and ExecutionContext(model_id='1e2ff5c0db8a4015ad3ee3d512ae0e80', should_add_diagnostic_data=False, is_finetuning=False, node_name=None).
2025-02-18 17:49:18 DEBUG    rasa.engine.graph  - Node 'rule_only_data_provider' running 'RuleOnlyDataProvider.provide'.
2025-02-18 17:49:18 DEBUG    rasa.engine.graph  - Node 'domain_provider' running 'DomainProvider.provide_inference'.
2025-02-18 17:49:18 DEBUG    rasa.engine.graph  - Node 'run_MemoizationPolicy0' running 'MemoizationPolicy.predict_action_probabilities'.
2025-02-18 17:49:18 DEBUG    rasa.core.policies.memoization  - [debug    ] memoization.predict.actions    tracker_states=[{'user': {'intent': 'ask_architecture'}, 'prev_action': {'action_name': 'action_listen'}}, {'user': {'intent': 'ask_architecture'}, 'prev_action': {'action_name': 'utter_architecture_response'}}]
2025-02-18 17:49:18 DEBUG    rasa.core.policies.memoization  - There is a memorised next action 'action_listen'
2025-02-18 17:49:18 DEBUG    rasa.engine.graph  - Node 'run_RulePolicy1' running 'RulePolicy.predict_action_probabilities'.
2025-02-18 17:49:18 DEBUG    rasa.core.policies.rule_policy  - [debug    ] rule_policy.actions.find       current_states=
[state 1] user intent: ask_architecture | previous action name: action_listen
[state 2] user intent: ask_architecture | previous action name: utter_architecture_response
[state 3] user intent: ask_architecture | previous action name: action_listen
[state 4] user intent: ask_architecture | previous action name: utter_architecture_response
2025-02-18 17:49:18 DEBUG    rasa.core.policies.rule_policy  - There is a rule for the next action 'action_listen'.
2025-02-18 17:49:18 DEBUG    rasa.engine.graph  - Node 'run_TEDPolicy2' running 'TEDPolicy.predict_action_probabilities'.
2025-02-18 17:49:18 DEBUG    rasa.core.policies.ted_policy  - TED predicted 'action_listen' based on user intent.
2025-02-18 17:49:18 DEBUG    rasa.engine.graph  - Node 'select_prediction' running 'DefaultPolicyPredictionEnsemble.combine_predictions_from_kwargs'.
2025-02-18 17:49:18 DEBUG    rasa.core.policies.ensemble  - Predicted next action using RulePolicy.
2025-02-18 17:49:18 DEBUG    rasa.core.processor  - Predicted next action 'action_listen' with confidence 1.00.
2025-02-18 17:49:18 DEBUG    rasa.core.processor  - [debug    ] processor.actions.policy_prediction prediction_events=[]
2025-02-18 17:49:18 DEBUG    rasa.core.processor  - [debug    ] processor.actions.log          action_name=action_listen rasa_events=[]
2025-02-18 17:49:18 DEBUG    rasa.core.tracker_store  - No event broker configured. Skipping streaming events.
2025-02-18 17:49:18 DEBUG    rasa.core.lock_store  - Deleted lock for conversation 'PractikumStudent'.
2025-02-18 17:49:24 DEBUG    rasa.core.lock_store  - Issuing ticket for conversation 'PractikumStudent'.
2025-02-18 17:49:24 DEBUG    rasa.core.lock_store  - Acquiring lock for conversation 'PractikumStudent'.
2025-02-18 17:49:24 DEBUG    rasa.core.lock_store  - Acquired lock for conversation 'PractikumStudent'.
2025-02-18 17:49:24 DEBUG    rasa.core.tracker_store  - Recreating tracker for id 'PractikumStudent'
2025-02-18 17:49:24 DEBUG    rasa.engine.runner.dask  - Running graph with inputs: {'__message__': [<rasa.core.channels.channel.UserMessage object at 0x0000024F273EBD60>], '__tracker__': <rasa.shared.core.trackers.DialogueStateTracker object at 0x0000024F2B4DC400>}, targets: ['run_RegexMessageHandler'] and ExecutionContext(model_id='1e2ff5c0db8a4015ad3ee3d512ae0e80', should_add_diagnostic_data=False, is_finetuning=False, node_name=None).
2025-02-18 17:49:24 DEBUG    rasa.engine.graph  - Node 'nlu_message_converter' running 'NLUMessageConverter.convert_user_message'.
2025-02-18 17:49:24 DEBUG    rasa.engine.graph  - Node 'run_WhitespaceTokenizer0' running 'WhitespaceTokenizer.process'.
2025-02-18 17:49:24 DEBUG    rasa.engine.graph  - Node 'run_RegexFeaturizer1' running 'RegexFeaturizer.process'.
2025-02-18 17:49:24 DEBUG    rasa.engine.graph  - Node 'run_LexicalSyntacticFeaturizer2' running 'LexicalSyntacticFeaturizer.process'.
2025-02-18 17:49:24 DEBUG    rasa.engine.graph  - Node 'run_CountVectorsFeaturizer3' running 'CountVectorsFeaturizer.process'.
2025-02-18 17:49:24 DEBUG    rasa.engine.graph  - Node 'run_LanguageModelFeaturizer4' running 'LanguageModelFeaturizer.process'.
2025-02-18 17:49:24 DEBUG    rasa.engine.graph  - Node 'run_DIETClassifier5' running 'DIETClassifier.process'.
2025-02-18 17:49:24 DEBUG    rasa.engine.graph  - Node 'run_EntitySynonymMapper6' running 'EntitySynonymMapper.process'.
2025-02-18 17:49:24 DEBUG    rasa.engine.graph  - Node 'run_ResponseSelector7' running 'ResponseSelector.process'.
2025-02-18 17:49:24 DEBUG    rasa.nlu.classifiers.diet_classifier  - There is no trained model for 'ResponseSelector': The component is either not trained or didn't receive enough training data.
2025-02-18 17:49:24 DEBUG    rasa.nlu.selectors.response_selector  - Adding following selector key to message property: default
2025-02-18 17:49:24 DEBUG    rasa.engine.graph  - Node 'domain_provider' running 'DomainProvider.provide_inference'.
2025-02-18 17:49:24 DEBUG    rasa.engine.graph  - Node 'run_RegexMessageHandler' running 'RegexMessageHandler.process'.
2025-02-18 17:49:24 DEBUG    rasa.core.processor  - [debug    ] processor.message.parse        parse_data_entities=[] parse_data_intent={'name': 'ask_architecture', 'confidence': 0.2737807631492615} parse_data_text=Пока
2025-02-18 17:49:24 DEBUG    rasa.core.processor  - Logged UserUtterance - tracker now has 16 events.
2025-02-18 17:49:24 DEBUG    rasa.core.actions.action  - Validating extracted slots: topic
2025-02-18 17:49:24 DEBUG    rasa.core.processor  - [debug    ] processor.extract.slots        action_extract_slot=action_extract_slots len_extraction_events=1 rasa_events=[SlotSet(key: topic, value: Пока)]
2025-02-18 17:49:24 DEBUG    rasa.engine.runner.dask  - Running graph with inputs: {'__tracker__': <rasa.shared.core.trackers.DialogueStateTracker object at 0x0000024F2B4DC400>}, targets: ['select_prediction'] and ExecutionContext(model_id='1e2ff5c0db8a4015ad3ee3d512ae0e80', should_add_diagnostic_data=False, is_finetuning=False, node_name=None).
2025-02-18 17:49:24 DEBUG    rasa.engine.graph  - Node 'rule_only_data_provider' running 'RuleOnlyDataProvider.provide'.
2025-02-18 17:49:24 DEBUG    rasa.engine.graph  - Node 'domain_provider' running 'DomainProvider.provide_inference'.
2025-02-18 17:49:24 DEBUG    rasa.engine.graph  - Node 'run_MemoizationPolicy0' running 'MemoizationPolicy.predict_action_probabilities'.
2025-02-18 17:49:24 DEBUG    rasa.core.policies.memoization  - [debug    ] memoization.predict.actions    tracker_states=[{'user': {'intent': 'ask_architecture'}, 'prev_action': {'action_name': 'utter_architecture_response'}}, {'user': {'intent': 'ask_architecture'}, 'prev_action': {'action_name': 'action_listen'}}]
2025-02-18 17:49:24 DEBUG    rasa.core.policies.memoization  - There is no memorised next action
2025-02-18 17:49:24 DEBUG    rasa.engine.graph  - Node 'run_RulePolicy1' running 'RulePolicy.predict_action_probabilities'.
2025-02-18 17:49:24 DEBUG    rasa.core.policies.rule_policy  - [debug    ] rule_policy.actions.find       current_states=
[state 1] user intent: ask_architecture | previous action name: action_listen
[state 2] user intent: ask_architecture | previous action name: utter_architecture_response
[state 3] user intent: ask_architecture | previous action name: action_listen
[state 4] user intent: ask_architecture | previous action name: utter_architecture_response
[state 5] user text: Пока | previous action name: action_listen
2025-02-18 17:49:24 DEBUG    rasa.core.policies.rule_policy  - There is no applicable rule.
2025-02-18 17:49:24 DEBUG    rasa.core.policies.rule_policy  - [debug    ] rule_policy.actions.find       current_states=
[state 1] user intent: ask_architecture | previous action name: action_listen
[state 2] user intent: ask_architecture | previous action name: utter_architecture_response
[state 3] user intent: ask_architecture | previous action name: action_listen
[state 4] user intent: ask_architecture | previous action name: utter_architecture_response
[state 5] user intent: ask_architecture | previous action name: action_listen
2025-02-18 17:49:24 DEBUG    rasa.core.policies.rule_policy  - There is a rule for the next action 'utter_architecture_response'.
2025-02-18 17:49:24 DEBUG    rasa.engine.graph  - Node 'run_TEDPolicy2' running 'TEDPolicy.predict_action_probabilities'.
2025-02-18 17:49:24 DEBUG    rasa.core.policies.ted_policy  - TED predicted 'action_deactivate_loop' based on user intent.
2025-02-18 17:49:24 DEBUG    rasa.engine.graph  - Node 'select_prediction' running 'DefaultPolicyPredictionEnsemble.combine_predictions_from_kwargs'.
2025-02-18 17:49:24 DEBUG    rasa.core.policies.ensemble  - Made prediction using user intent.
2025-02-18 17:49:24 DEBUG    rasa.core.policies.ensemble  - Added `DefinePrevUserUtteredFeaturization(False)` event.
2025-02-18 17:49:24 DEBUG    rasa.core.policies.ensemble  - Predicted next action using RulePolicy.
2025-02-18 17:49:24 DEBUG    rasa.core.processor  - Predicted next action 'utter_architecture_response' with confidence 1.00.
2025-02-18 17:49:24 DEBUG    rasa.core.processor  - [debug    ] processor.actions.policy_prediction prediction_events=[<rasa.shared.core.events.DefinePrevUserUtteredFeaturization object at 0x0000024F2B489960>]
2025-02-18 17:49:24 DEBUG    rasa.core.processor  - [debug    ] processor.actions.log          action_name=utter_architecture_response rasa_events=[BotUttered('Архитектура ПО включает выбор структур, которые обеспечивают масштабируемость, гибкость и поддерживаемость приложения. Задайте конкретный вопрос по этой теме, и я помогу вам с информацией.', {"elements": null, "quick_replies": null, "buttons": null, "attachment": null, "image": null, "custom": null}, {"utter_action": "utter_architecture_response"}, 1739890164.8864393)]
2025-02-18 17:49:24 DEBUG    rasa.engine.runner.dask  - Running graph with inputs: {'__tracker__': <rasa.shared.core.trackers.DialogueStateTracker object at 0x0000024F2B4DC400>}, targets: ['select_prediction'] and ExecutionContext(model_id='1e2ff5c0db8a4015ad3ee3d512ae0e80', should_add_diagnostic_data=False, is_finetuning=False, node_name=None).
2025-02-18 17:49:24 DEBUG    rasa.engine.graph  - Node 'rule_only_data_provider' running 'RuleOnlyDataProvider.provide'.
2025-02-18 17:49:24 DEBUG    rasa.engine.graph  - Node 'domain_provider' running 'DomainProvider.provide_inference'.
2025-02-18 17:49:24 DEBUG    rasa.engine.graph  - Node 'run_MemoizationPolicy0' running 'MemoizationPolicy.predict_action_probabilities'.
2025-02-18 17:49:24 DEBUG    rasa.core.policies.memoization  - [debug    ] memoization.predict.actions    tracker_states=[{'user': {'intent': 'ask_architecture'}, 'prev_action': {'action_name': 'action_listen'}}, {'user': {'intent': 'ask_architecture'}, 'prev_action': {'action_name': 'utter_architecture_response'}}]
2025-02-18 17:49:24 DEBUG    rasa.core.policies.memoization  - There is a memorised next action 'action_listen'
2025-02-18 17:49:24 DEBUG    rasa.engine.graph  - Node 'run_RulePolicy1' running 'RulePolicy.predict_action_probabilities'.
2025-02-18 17:49:24 DEBUG    rasa.core.policies.rule_policy  - [debug    ] rule_policy.actions.find       current_states=
[state 1] user intent: ask_architecture | previous action name: action_listen
[state 2] user intent: ask_architecture | previous action name: utter_architecture_response
[state 3] user intent: ask_architecture | previous action name: action_listen
[state 4] user intent: ask_architecture | previous action name: utter_architecture_response
[state 5] user intent: ask_architecture | previous action name: action_listen
[state 6] user intent: ask_architecture | previous action name: utter_architecture_response
2025-02-18 17:49:24 DEBUG    rasa.core.policies.rule_policy  - There is a rule for the next action 'action_listen'.
2025-02-18 17:49:24 DEBUG    rasa.engine.graph  - Node 'run_TEDPolicy2' running 'TEDPolicy.predict_action_probabilities'.
2025-02-18 17:49:24 DEBUG    rasa.core.policies.ted_policy  - TED predicted 'action_listen' based on user intent.
2025-02-18 17:49:24 DEBUG    rasa.engine.graph  - Node 'select_prediction' running 'DefaultPolicyPredictionEnsemble.combine_predictions_from_kwargs'.
2025-02-18 17:49:24 DEBUG    rasa.core.policies.ensemble  - Predicted next action using RulePolicy.
2025-02-18 17:49:24 DEBUG    rasa.core.processor  - Predicted next action 'action_listen' with confidence 1.00.
2025-02-18 17:49:24 DEBUG    rasa.core.processor  - [debug    ] processor.actions.policy_prediction prediction_events=[]
2025-02-18 17:49:24 DEBUG    rasa.core.processor  - [debug    ] processor.actions.log          action_name=action_listen rasa_events=[]
2025-02-18 17:49:24 DEBUG    rasa.core.tracker_store  - No event broker configured. Skipping streaming events.
2025-02-18 17:49:24 DEBUG    rasa.core.lock_store  - Deleted lock for conversation 'PractikumStudent'.
2025-02-18 17:49:32 DEBUG    rasa.core.lock_store  - Issuing ticket for conversation 'PractikumStudent'.
2025-02-18 17:49:32 DEBUG    rasa.core.lock_store  - Acquiring lock for conversation 'PractikumStudent'.
2025-02-18 17:49:32 DEBUG    rasa.core.lock_store  - Acquired lock for conversation 'PractikumStudent'.
2025-02-18 17:49:32 DEBUG    rasa.core.tracker_store  - Recreating tracker for id 'PractikumStudent'
2025-02-18 17:49:32 DEBUG    rasa.engine.runner.dask  - Running graph with inputs: {'__message__': [<rasa.core.channels.channel.UserMessage object at 0x0000024F25FD5FF0>], '__tracker__': <rasa.shared.core.trackers.DialogueStateTracker object at 0x0000024F1F171240>}, targets: ['run_RegexMessageHandler'] and ExecutionContext(model_id='1e2ff5c0db8a4015ad3ee3d512ae0e80', should_add_diagnostic_data=False, is_finetuning=False, node_name=None).
2025-02-18 17:49:32 DEBUG    rasa.engine.graph  - Node 'nlu_message_converter' running 'NLUMessageConverter.convert_user_message'.
2025-02-18 17:49:32 DEBUG    rasa.engine.graph  - Node 'run_WhitespaceTokenizer0' running 'WhitespaceTokenizer.process'.
2025-02-18 17:49:32 DEBUG    rasa.engine.graph  - Node 'run_RegexFeaturizer1' running 'RegexFeaturizer.process'.
2025-02-18 17:49:32 DEBUG    rasa.engine.graph  - Node 'run_LexicalSyntacticFeaturizer2' running 'LexicalSyntacticFeaturizer.process'.
2025-02-18 17:49:32 DEBUG    rasa.engine.graph  - Node 'run_CountVectorsFeaturizer3' running 'CountVectorsFeaturizer.process'.
2025-02-18 17:49:32 DEBUG    rasa.engine.graph  - Node 'run_LanguageModelFeaturizer4' running 'LanguageModelFeaturizer.process'.
2025-02-18 17:49:32 DEBUG    rasa.engine.graph  - Node 'run_DIETClassifier5' running 'DIETClassifier.process'.
2025-02-18 17:49:32 DEBUG    rasa.engine.graph  - Node 'run_EntitySynonymMapper6' running 'EntitySynonymMapper.process'.
2025-02-18 17:49:32 DEBUG    rasa.engine.graph  - Node 'run_ResponseSelector7' running 'ResponseSelector.process'.
2025-02-18 17:49:32 DEBUG    rasa.nlu.classifiers.diet_classifier  - There is no trained model for 'ResponseSelector': The component is either not trained or didn't receive enough training data.
2025-02-18 17:49:32 DEBUG    rasa.nlu.selectors.response_selector  - Adding following selector key to message property: default
2025-02-18 17:49:32 DEBUG    rasa.engine.graph  - Node 'domain_provider' running 'DomainProvider.provide_inference'.
2025-02-18 17:49:32 DEBUG    rasa.engine.graph  - Node 'run_RegexMessageHandler' running 'RegexMessageHandler.process'.
2025-02-18 17:49:32 DEBUG    rasa.core.processor  - [debug    ] processor.message.parse        parse_data_entities=[] parse_data_intent={'name': 'deny', 'confidence': 0.2794873118400574} parse_data_text=Добрый день
2025-02-18 17:49:32 DEBUG    rasa.core.processor  - Logged UserUtterance - tracker now has 22 events.
2025-02-18 17:49:32 DEBUG    rasa.core.actions.action  - Validating extracted slots: topic
2025-02-18 17:49:32 DEBUG    rasa.core.processor  - [debug    ] processor.extract.slots        action_extract_slot=action_extract_slots len_extraction_events=1 rasa_events=[SlotSet(key: topic, value: Добрый день)]
2025-02-18 17:49:32 DEBUG    rasa.engine.runner.dask  - Running graph with inputs: {'__tracker__': <rasa.shared.core.trackers.DialogueStateTracker object at 0x0000024F1F171240>}, targets: ['select_prediction'] and ExecutionContext(model_id='1e2ff5c0db8a4015ad3ee3d512ae0e80', should_add_diagnostic_data=False, is_finetuning=False, node_name=None).
2025-02-18 17:49:32 DEBUG    rasa.engine.graph  - Node 'rule_only_data_provider' running 'RuleOnlyDataProvider.provide'.
2025-02-18 17:49:32 DEBUG    rasa.engine.graph  - Node 'domain_provider' running 'DomainProvider.provide_inference'.
2025-02-18 17:49:32 DEBUG    rasa.engine.graph  - Node 'run_MemoizationPolicy0' running 'MemoizationPolicy.predict_action_probabilities'.
2025-02-18 17:49:32 DEBUG    rasa.core.policies.memoization  - [debug    ] memoization.predict.actions    tracker_states=[{'user': {'intent': 'ask_architecture'}, 'prev_action': {'action_name': 'utter_architecture_response'}}, {'user': {'intent': 'deny'}, 'prev_action': {'action_name': 'action_listen'}}]
2025-02-18 17:49:32 DEBUG    rasa.core.policies.memoization  - There is no memorised next action
2025-02-18 17:49:32 DEBUG    rasa.engine.graph  - Node 'run_RulePolicy1' running 'RulePolicy.predict_action_probabilities'.
2025-02-18 17:49:32 DEBUG    rasa.core.policies.rule_policy  - [debug    ] rule_policy.actions.find       current_states=
[state 1] user intent: ask_architecture | previous action name: action_listen
[state 2] user intent: ask_architecture | previous action name: utter_architecture_response
[state 3] user intent: ask_architecture | previous action name: action_listen
[state 4] user intent: ask_architecture | previous action name: utter_architecture_response
[state 5] user intent: ask_architecture | previous action name: action_listen
[state 6] user intent: ask_architecture | previous action name: utter_architecture_response
[state 7] user text: Добрый день | previous action name: action_listen
2025-02-18 17:49:32 DEBUG    rasa.core.policies.rule_policy  - There is no applicable rule.
2025-02-18 17:49:32 DEBUG    rasa.core.policies.rule_policy  - [debug    ] rule_policy.actions.find       current_states=
[state 1] user intent: ask_architecture | previous action name: action_listen
[state 2] user intent: ask_architecture | previous action name: utter_architecture_response
[state 3] user intent: ask_architecture | previous action name: action_listen
[state 4] user intent: ask_architecture | previous action name: utter_architecture_response
[state 5] user intent: ask_architecture | previous action name: action_listen
[state 6] user intent: ask_architecture | previous action name: utter_architecture_response
[state 7] user intent: deny | previous action name: action_listen
2025-02-18 17:49:32 DEBUG    rasa.core.policies.rule_policy  - There is no applicable rule.
2025-02-18 17:49:32 DEBUG    rasa.engine.graph  - Node 'run_TEDPolicy2' running 'TEDPolicy.predict_action_probabilities'.
2025-02-18 17:49:32 DEBUG    rasa.core.policies.ted_policy  - TED predicted 'utter_ask_more' based on user intent.
2025-02-18 17:49:32 DEBUG    rasa.engine.graph  - Node 'select_prediction' running 'DefaultPolicyPredictionEnsemble.combine_predictions_from_kwargs'.
2025-02-18 17:49:32 DEBUG    rasa.core.policies.ensemble  - Made prediction using user intent.
2025-02-18 17:49:32 DEBUG    rasa.core.policies.ensemble  - Added `DefinePrevUserUtteredFeaturization(False)` event.
2025-02-18 17:49:32 DEBUG    rasa.core.policies.ensemble  - Predicted next action using RulePolicy.
2025-02-18 17:49:32 DEBUG    rasa.core.processor  - Predicted next action 'action_default_fallback' with confidence 0.30.
2025-02-18 17:49:32 DEBUG    rasa.core.processor  - [debug    ] processor.actions.policy_prediction prediction_events=[<rasa.shared.core.events.DefinePrevUserUtteredFeaturization object at 0x0000024F2B48A470>]
2025-02-18 17:49:32 DEBUG    rasa.core.processor  - [debug    ] processor.actions.log          action_name=action_default_fallback rasa_events=[<rasa.shared.core.events.UserUtteranceReverted object at 0x0000024F2B48A800>]
2025-02-18 17:49:32 DEBUG    rasa.core.processor  - [debug    ] processor.slots.log            slot_values=     topic: Пока
session_started_metadata: None
2025-02-18 17:49:32 DEBUG    rasa.engine.runner.dask  - Running graph with inputs: {'__tracker__': <rasa.shared.core.trackers.DialogueStateTracker object at 0x0000024F1F171240>}, targets: ['select_prediction'] and ExecutionContext(model_id='1e2ff5c0db8a4015ad3ee3d512ae0e80', should_add_diagnostic_data=False, is_finetuning=False, node_name=None).
2025-02-18 17:49:32 DEBUG    rasa.engine.graph  - Node 'rule_only_data_provider' running 'RuleOnlyDataProvider.provide'.
2025-02-18 17:49:32 DEBUG    rasa.engine.graph  - Node 'domain_provider' running 'DomainProvider.provide_inference'.
2025-02-18 17:49:32 DEBUG    rasa.engine.graph  - Node 'run_MemoizationPolicy0' running 'MemoizationPolicy.predict_action_probabilities'.
2025-02-18 17:49:32 DEBUG    rasa.core.policies.memoization  - [debug    ] memoization.predict.actions    tracker_states=[{'user': {'intent': 'ask_architecture'}, 'prev_action': {'action_name': 'action_listen'}}, {'user': {'intent': 'ask_architecture'}, 'prev_action': {'action_name': 'utter_architecture_response'}}]
2025-02-18 17:49:32 DEBUG    rasa.core.policies.memoization  - There is a memorised next action 'action_listen'
2025-02-18 17:49:32 DEBUG    rasa.engine.graph  - Node 'run_RulePolicy1' running 'RulePolicy.predict_action_probabilities'.
2025-02-18 17:49:32 DEBUG    rasa.core.policies.rule_policy  - [debug    ] rule_policy.actions.find       current_states=
[state 1] user intent: ask_architecture | previous action name: action_listen
[state 2] user intent: ask_architecture | previous action name: utter_architecture_response
[state 3] user intent: ask_architecture | previous action name: action_listen
[state 4] user intent: ask_architecture | previous action name: utter_architecture_response
[state 5] user intent: ask_architecture | previous action name: action_listen
[state 6] user intent: ask_architecture | previous action name: utter_architecture_response
2025-02-18 17:49:32 DEBUG    rasa.core.policies.rule_policy  - There is a rule for the next action 'action_listen'.
2025-02-18 17:49:32 DEBUG    rasa.engine.graph  - Node 'run_TEDPolicy2' running 'TEDPolicy.predict_action_probabilities'.
2025-02-18 17:49:32 DEBUG    rasa.core.policies.ted_policy  - TED predicted 'action_listen' based on user intent.
2025-02-18 17:49:32 DEBUG    rasa.engine.graph  - Node 'select_prediction' running 'DefaultPolicyPredictionEnsemble.combine_predictions_from_kwargs'.
2025-02-18 17:49:32 DEBUG    rasa.core.policies.ensemble  - Predicted next action using RulePolicy.
2025-02-18 17:49:32 DEBUG    rasa.core.processor  - Predicted next action 'action_listen' with confidence 1.00.
2025-02-18 17:49:32 DEBUG    rasa.core.processor  - [debug    ] processor.actions.policy_prediction prediction_events=[]
2025-02-18 17:49:32 DEBUG    rasa.core.processor  - [debug    ] processor.actions.log          action_name=action_listen rasa_events=[]
2025-02-18 17:49:32 DEBUG    rasa.core.tracker_store  - No event broker configured. Skipping streaming events.
2025-02-18 17:49:32 DEBUG    rasa.core.lock_store  - Deleted lock for conversation 'PractikumStudent'.
2025-02-18 17:49:44 DEBUG    rasa.core.lock_store  - Issuing ticket for conversation 'PractikumStudent'.
2025-02-18 17:49:44 DEBUG    rasa.core.lock_store  - Acquiring lock for conversation 'PractikumStudent'.
2025-02-18 17:49:44 DEBUG    rasa.core.lock_store  - Acquired lock for conversation 'PractikumStudent'.
2025-02-18 17:49:44 DEBUG    rasa.core.tracker_store  - Recreating tracker for id 'PractikumStudent'
2025-02-18 17:49:44 DEBUG    rasa.engine.runner.dask  - Running graph with inputs: {'__message__': [<rasa.core.channels.channel.UserMessage object at 0x0000024F25FD5FF0>], '__tracker__': <rasa.shared.core.trackers.DialogueStateTracker object at 0x0000024F2B4DD360>}, targets: ['run_RegexMessageHandler'] and ExecutionContext(model_id='1e2ff5c0db8a4015ad3ee3d512ae0e80', should_add_diagnostic_data=False, is_finetuning=False, node_name=None).
2025-02-18 17:49:44 DEBUG    rasa.engine.graph  - Node 'nlu_message_converter' running 'NLUMessageConverter.convert_user_message'.
2025-02-18 17:49:44 DEBUG    rasa.engine.graph  - Node 'run_WhitespaceTokenizer0' running 'WhitespaceTokenizer.process'.
2025-02-18 17:49:44 DEBUG    rasa.engine.graph  - Node 'run_RegexFeaturizer1' running 'RegexFeaturizer.process'.
2025-02-18 17:49:44 DEBUG    rasa.engine.graph  - Node 'run_LexicalSyntacticFeaturizer2' running 'LexicalSyntacticFeaturizer.process'.
2025-02-18 17:49:44 DEBUG    rasa.engine.graph  - Node 'run_CountVectorsFeaturizer3' running 'CountVectorsFeaturizer.process'.
2025-02-18 17:49:44 DEBUG    rasa.engine.graph  - Node 'run_LanguageModelFeaturizer4' running 'LanguageModelFeaturizer.process'.
2025-02-18 17:49:44 DEBUG    rasa.engine.graph  - Node 'run_DIETClassifier5' running 'DIETClassifier.process'.
2025-02-18 17:49:44 DEBUG    rasa.engine.graph  - Node 'run_EntitySynonymMapper6' running 'EntitySynonymMapper.process'.
2025-02-18 17:49:44 DEBUG    rasa.engine.graph  - Node 'run_ResponseSelector7' running 'ResponseSelector.process'.
2025-02-18 17:49:44 DEBUG    rasa.nlu.classifiers.diet_classifier  - There is no trained model for 'ResponseSelector': The component is either not trained or didn't receive enough training data.
2025-02-18 17:49:44 DEBUG    rasa.nlu.selectors.response_selector  - Adding following selector key to message property: default
2025-02-18 17:49:44 DEBUG    rasa.engine.graph  - Node 'domain_provider' running 'DomainProvider.provide_inference'.
2025-02-18 17:49:44 DEBUG    rasa.engine.graph  - Node 'run_RegexMessageHandler' running 'RegexMessageHandler.process'.
2025-02-18 17:49:44 DEBUG    rasa.core.processor  - [debug    ] processor.message.parse        parse_data_entities=[] parse_data_intent={'name': 'ask_architecture', 'confidence': 0.2588994801044464} parse_data_text=Архитектура
2025-02-18 17:49:44 DEBUG    rasa.core.processor  - Logged UserUtterance - tracker now has 28 events.
2025-02-18 17:49:44 DEBUG    rasa.core.actions.action  - Validating extracted slots: topic
2025-02-18 17:49:44 DEBUG    rasa.core.processor  - [debug    ] processor.extract.slots        action_extract_slot=action_extract_slots len_extraction_events=1 rasa_events=[SlotSet(key: topic, value: Архитектура)]
2025-02-18 17:49:44 DEBUG    rasa.engine.runner.dask  - Running graph with inputs: {'__tracker__': <rasa.shared.core.trackers.DialogueStateTracker object at 0x0000024F2B4DD360>}, targets: ['select_prediction'] and ExecutionContext(model_id='1e2ff5c0db8a4015ad3ee3d512ae0e80', should_add_diagnostic_data=False, is_finetuning=False, node_name=None).
2025-02-18 17:49:44 DEBUG    rasa.engine.graph  - Node 'rule_only_data_provider' running 'RuleOnlyDataProvider.provide'.
2025-02-18 17:49:44 DEBUG    rasa.engine.graph  - Node 'domain_provider' running 'DomainProvider.provide_inference'.
2025-02-18 17:49:44 DEBUG    rasa.engine.graph  - Node 'run_MemoizationPolicy0' running 'MemoizationPolicy.predict_action_probabilities'.
2025-02-18 17:49:44 DEBUG    rasa.core.policies.memoization  - [debug    ] memoization.predict.actions    tracker_states=[{'user': {'intent': 'ask_architecture'}, 'prev_action': {'action_name': 'utter_architecture_response'}}, {'user': {'intent': 'ask_architecture'}, 'prev_action': {'action_name': 'action_listen'}}]
2025-02-18 17:49:44 DEBUG    rasa.core.policies.memoization  - There is no memorised next action
2025-02-18 17:49:44 DEBUG    rasa.engine.graph  - Node 'run_RulePolicy1' running 'RulePolicy.predict_action_probabilities'.
2025-02-18 17:49:44 DEBUG    rasa.core.policies.rule_policy  - [debug    ] rule_policy.actions.find       current_states=
[state 1] user intent: ask_architecture | previous action name: action_listen
[state 2] user intent: ask_architecture | previous action name: utter_architecture_response
[state 3] user intent: ask_architecture | previous action name: action_listen
[state 4] user intent: ask_architecture | previous action name: utter_architecture_response
[state 5] user intent: ask_architecture | previous action name: action_listen
[state 6] user intent: ask_architecture | previous action name: utter_architecture_response
[state 7] user text: Архитектура | previous action name: action_listen
2025-02-18 17:49:44 DEBUG    rasa.core.policies.rule_policy  - There is no applicable rule.
2025-02-18 17:49:44 DEBUG    rasa.core.policies.rule_policy  - [debug    ] rule_policy.actions.find       current_states=
[state 1] user intent: ask_architecture | previous action name: action_listen
[state 2] user intent: ask_architecture | previous action name: utter_architecture_response
[state 3] user intent: ask_architecture | previous action name: action_listen
[state 4] user intent: ask_architecture | previous action name: utter_architecture_response
[state 5] user intent: ask_architecture | previous action name: action_listen
[state 6] user intent: ask_architecture | previous action name: utter_architecture_response
[state 7] user intent: ask_architecture | previous action name: action_listen
2025-02-18 17:49:44 DEBUG    rasa.core.policies.rule_policy  - There is a rule for the next action 'utter_architecture_response'.
2025-02-18 17:49:44 DEBUG    rasa.engine.graph  - Node 'run_TEDPolicy2' running 'TEDPolicy.predict_action_probabilities'.
2025-02-18 17:49:44 DEBUG    rasa.core.policies.ted_policy  - TED predicted 'action_deactivate_loop' based on user intent.
2025-02-18 17:49:44 DEBUG    rasa.engine.graph  - Node 'select_prediction' running 'DefaultPolicyPredictionEnsemble.combine_predictions_from_kwargs'.
2025-02-18 17:49:44 DEBUG    rasa.core.policies.ensemble  - Made prediction using user intent.
2025-02-18 17:49:44 DEBUG    rasa.core.policies.ensemble  - Added `DefinePrevUserUtteredFeaturization(False)` event.
2025-02-18 17:49:44 DEBUG    rasa.core.policies.ensemble  - Predicted next action using RulePolicy.
2025-02-18 17:49:44 DEBUG    rasa.core.processor  - Predicted next action 'utter_architecture_response' with confidence 1.00.
2025-02-18 17:49:44 DEBUG    rasa.core.processor  - [debug    ] processor.actions.policy_prediction prediction_events=[<rasa.shared.core.events.DefinePrevUserUtteredFeaturization object at 0x0000024F2B48BF70>]
2025-02-18 17:49:44 DEBUG    rasa.core.processor  - [debug    ] processor.actions.log          action_name=utter_architecture_response rasa_events=[BotUttered('Архитектура ПО включает выбор структур, которые обеспечивают масштабируемость, гибкость и поддерживаемость приложения. Задайте конкретный вопрос по этой теме, и я помогу вам с информацией.', {"elements": null, "quick_replies": null, "buttons": null, "attachment": null, "image": null, "custom": null}, {"utter_action": "utter_architecture_response"}, 1739890184.566704)]
2025-02-18 17:49:44 DEBUG    rasa.engine.runner.dask  - Running graph with inputs: {'__tracker__': <rasa.shared.core.trackers.DialogueStateTracker object at 0x0000024F2B4DD360>}, targets: ['select_prediction'] and ExecutionContext(model_id='1e2ff5c0db8a4015ad3ee3d512ae0e80', should_add_diagnostic_data=False, is_finetuning=False, node_name=None).
2025-02-18 17:49:44 DEBUG    rasa.engine.graph  - Node 'rule_only_data_provider' running 'RuleOnlyDataProvider.provide'.
2025-02-18 17:49:44 DEBUG    rasa.engine.graph  - Node 'domain_provider' running 'DomainProvider.provide_inference'.
2025-02-18 17:49:44 DEBUG    rasa.engine.graph  - Node 'run_MemoizationPolicy0' running 'MemoizationPolicy.predict_action_probabilities'.
2025-02-18 17:49:44 DEBUG    rasa.core.policies.memoization  - [debug    ] memoization.predict.actions    tracker_states=[{'user': {'intent': 'ask_architecture'}, 'prev_action': {'action_name': 'action_listen'}}, {'user': {'intent': 'ask_architecture'}, 'prev_action': {'action_name': 'utter_architecture_response'}}]
2025-02-18 17:49:44 DEBUG    rasa.core.policies.memoization  - There is a memorised next action 'action_listen'
2025-02-18 17:49:44 DEBUG    rasa.engine.graph  - Node 'run_RulePolicy1' running 'RulePolicy.predict_action_probabilities'.
2025-02-18 17:49:44 DEBUG    rasa.core.policies.rule_policy  - [debug    ] rule_policy.actions.find       current_states=
[state 1] user intent: ask_architecture | previous action name: action_listen
[state 2] user intent: ask_architecture | previous action name: utter_architecture_response
[state 3] user intent: ask_architecture | previous action name: action_listen
[state 4] user intent: ask_architecture | previous action name: utter_architecture_response
[state 5] user intent: ask_architecture | previous action name: action_listen
[state 6] user intent: ask_architecture | previous action name: utter_architecture_response
[state 7] user intent: ask_architecture | previous action name: action_listen
[state 8] user intent: ask_architecture | previous action name: utter_architecture_response
2025-02-18 17:49:44 DEBUG    rasa.core.policies.rule_policy  - There is a rule for the next action 'action_listen'.
2025-02-18 17:49:44 DEBUG    rasa.engine.graph  - Node 'run_TEDPolicy2' running 'TEDPolicy.predict_action_probabilities'.
2025-02-18 17:49:44 DEBUG    rasa.core.policies.ted_policy  - TED predicted 'action_listen' based on user intent.
2025-02-18 17:49:44 DEBUG    rasa.engine.graph  - Node 'select_prediction' running 'DefaultPolicyPredictionEnsemble.combine_predictions_from_kwargs'.
2025-02-18 17:49:44 DEBUG    rasa.core.policies.ensemble  - Predicted next action using RulePolicy.
2025-02-18 17:49:44 DEBUG    rasa.core.processor  - Predicted next action 'action_listen' with confidence 1.00.
2025-02-18 17:49:44 DEBUG    rasa.core.processor  - [debug    ] processor.actions.policy_prediction prediction_events=[]
2025-02-18 17:49:44 DEBUG    rasa.core.processor  - [debug    ] processor.actions.log          action_name=action_listen rasa_events=[]
2025-02-18 17:49:44 DEBUG    rasa.core.tracker_store  - No event broker configured. Skipping streaming events.
2025-02-18 17:49:44 DEBUG    rasa.core.lock_store  - Deleted lock for conversation 'PractikumStudent'.
2025-02-18 17:49:49 DEBUG    rasa.core.lock_store  - Issuing ticket for conversation 'PractikumStudent'.
2025-02-18 17:49:49 DEBUG    rasa.core.lock_store  - Acquiring lock for conversation 'PractikumStudent'.
2025-02-18 17:49:49 DEBUG    rasa.core.lock_store  - Acquired lock for conversation 'PractikumStudent'.
2025-02-18 17:49:49 DEBUG    rasa.core.tracker_store  - Recreating tracker for id 'PractikumStudent'
2025-02-18 17:49:49 DEBUG    rasa.engine.runner.dask  - Running graph with inputs: {'__message__': [<rasa.core.channels.channel.UserMessage object at 0x0000024F25FD7610>], '__tracker__': <rasa.shared.core.trackers.DialogueStateTracker object at 0x0000024F2B4DC400>}, targets: ['run_RegexMessageHandler'] and ExecutionContext(model_id='1e2ff5c0db8a4015ad3ee3d512ae0e80', should_add_diagnostic_data=False, is_finetuning=False, node_name=None).
2025-02-18 17:49:49 DEBUG    rasa.engine.graph  - Node 'nlu_message_converter' running 'NLUMessageConverter.convert_user_message'.
2025-02-18 17:49:49 DEBUG    rasa.engine.graph  - Node 'run_WhitespaceTokenizer0' running 'WhitespaceTokenizer.process'.
2025-02-18 17:49:49 DEBUG    rasa.engine.graph  - Node 'run_RegexFeaturizer1' running 'RegexFeaturizer.process'.
2025-02-18 17:49:49 DEBUG    rasa.engine.graph  - Node 'run_LexicalSyntacticFeaturizer2' running 'LexicalSyntacticFeaturizer.process'.
2025-02-18 17:49:49 DEBUG    rasa.engine.graph  - Node 'run_CountVectorsFeaturizer3' running 'CountVectorsFeaturizer.process'.
2025-02-18 17:49:49 DEBUG    rasa.engine.graph  - Node 'run_LanguageModelFeaturizer4' running 'LanguageModelFeaturizer.process'.
2025-02-18 17:49:49 DEBUG    rasa.engine.graph  - Node 'run_DIETClassifier5' running 'DIETClassifier.process'.
2025-02-18 17:49:49 DEBUG    rasa.engine.graph  - Node 'run_EntitySynonymMapper6' running 'EntitySynonymMapper.process'.
2025-02-18 17:49:49 DEBUG    rasa.engine.graph  - Node 'run_ResponseSelector7' running 'ResponseSelector.process'.
2025-02-18 17:49:49 DEBUG    rasa.nlu.classifiers.diet_classifier  - There is no trained model for 'ResponseSelector': The component is either not trained or didn't receive enough training data.
2025-02-18 17:49:49 DEBUG    rasa.nlu.selectors.response_selector  - Adding following selector key to message property: default
2025-02-18 17:49:49 DEBUG    rasa.engine.graph  - Node 'domain_provider' running 'DomainProvider.provide_inference'.
2025-02-18 17:49:49 DEBUG    rasa.engine.graph  - Node 'run_RegexMessageHandler' running 'RegexMessageHandler.process'.
2025-02-18 17:49:49 DEBUG    rasa.core.processor  - [debug    ] processor.message.parse        parse_data_entities=[] parse_data_intent={'name': 'ask_architecture', 'confidence': 0.27118220925331116} parse_data_text=Привет
2025-02-18 17:49:49 DEBUG    rasa.core.processor  - Logged UserUtterance - tracker now has 34 events.
2025-02-18 17:49:49 DEBUG    rasa.core.actions.action  - Validating extracted slots: topic
2025-02-18 17:49:49 DEBUG    rasa.core.processor  - [debug    ] processor.extract.slots        action_extract_slot=action_extract_slots len_extraction_events=1 rasa_events=[SlotSet(key: topic, value: Привет)]
2025-02-18 17:49:49 DEBUG    rasa.engine.runner.dask  - Running graph with inputs: {'__tracker__': <rasa.shared.core.trackers.DialogueStateTracker object at 0x0000024F2B4DC400>}, targets: ['select_prediction'] and ExecutionContext(model_id='1e2ff5c0db8a4015ad3ee3d512ae0e80', should_add_diagnostic_data=False, is_finetuning=False, node_name=None).
2025-02-18 17:49:49 DEBUG    rasa.engine.graph  - Node 'rule_only_data_provider' running 'RuleOnlyDataProvider.provide'.
2025-02-18 17:49:49 DEBUG    rasa.engine.graph  - Node 'domain_provider' running 'DomainProvider.provide_inference'.
2025-02-18 17:49:49 DEBUG    rasa.engine.graph  - Node 'run_MemoizationPolicy0' running 'MemoizationPolicy.predict_action_probabilities'.
2025-02-18 17:49:49 DEBUG    rasa.core.policies.memoization  - [debug    ] memoization.predict.actions    tracker_states=[{'user': {'intent': 'ask_architecture'}, 'prev_action': {'action_name': 'utter_architecture_response'}}, {'user': {'intent': 'ask_architecture'}, 'prev_action': {'action_name': 'action_listen'}}]
2025-02-18 17:49:49 DEBUG    rasa.core.policies.memoization  - There is no memorised next action
2025-02-18 17:49:49 DEBUG    rasa.engine.graph  - Node 'run_RulePolicy1' running 'RulePolicy.predict_action_probabilities'.
2025-02-18 17:49:49 DEBUG    rasa.core.policies.rule_policy  - [debug    ] rule_policy.actions.find       current_states=
[state 1] user intent: ask_architecture | previous action name: action_listen
[state 2] user intent: ask_architecture | previous action name: utter_architecture_response
[state 3] user intent: ask_architecture | previous action name: action_listen
[state 4] user intent: ask_architecture | previous action name: utter_architecture_response
[state 5] user intent: ask_architecture | previous action name: action_listen
[state 6] user intent: ask_architecture | previous action name: utter_architecture_response
[state 7] user intent: ask_architecture | previous action name: action_listen
[state 8] user intent: ask_architecture | previous action name: utter_architecture_response
[state 9] user text: Привет | previous action name: action_listen
2025-02-18 17:49:49 DEBUG    rasa.core.policies.rule_policy  - There is no applicable rule.
2025-02-18 17:49:49 DEBUG    rasa.core.policies.rule_policy  - [debug    ] rule_policy.actions.find       current_states=
[state 1] user intent: ask_architecture | previous action name: action_listen
[state 2] user intent: ask_architecture | previous action name: utter_architecture_response
[state 3] user intent: ask_architecture | previous action name: action_listen
[state 4] user intent: ask_architecture | previous action name: utter_architecture_response
[state 5] user intent: ask_architecture | previous action name: action_listen
[state 6] user intent: ask_architecture | previous action name: utter_architecture_response
[state 7] user intent: ask_architecture | previous action name: action_listen
[state 8] user intent: ask_architecture | previous action name: utter_architecture_response
[state 9] user intent: ask_architecture | previous action name: action_listen
2025-02-18 17:49:49 DEBUG    rasa.core.policies.rule_policy  - There is a rule for the next action 'utter_architecture_response'.
2025-02-18 17:49:49 DEBUG    rasa.engine.graph  - Node 'run_TEDPolicy2' running 'TEDPolicy.predict_action_probabilities'.
2025-02-18 17:49:49 DEBUG    rasa.core.policies.ted_policy  - TED predicted 'action_deactivate_loop' based on user intent.
2025-02-18 17:49:49 DEBUG    rasa.engine.graph  - Node 'select_prediction' running 'DefaultPolicyPredictionEnsemble.combine_predictions_from_kwargs'.
2025-02-18 17:49:49 DEBUG    rasa.core.policies.ensemble  - Made prediction using user intent.
2025-02-18 17:49:49 DEBUG    rasa.core.policies.ensemble  - Added `DefinePrevUserUtteredFeaturization(False)` event.
2025-02-18 17:49:49 DEBUG    rasa.core.policies.ensemble  - Predicted next action using RulePolicy.
2025-02-18 17:49:49 DEBUG    rasa.core.processor  - Predicted next action 'utter_architecture_response' with confidence 1.00.
2025-02-18 17:49:49 DEBUG    rasa.core.processor  - [debug    ] processor.actions.policy_prediction prediction_events=[<rasa.shared.core.events.DefinePrevUserUtteredFeaturization object at 0x0000024F2B489A20>]
2025-02-18 17:49:49 DEBUG    rasa.core.processor  - [debug    ] processor.actions.log          action_name=utter_architecture_response rasa_events=[BotUttered('Архитектура ПО включает выбор структур, которые обеспечивают масштабируемость, гибкость и поддерживаемость приложения. Задайте конкретный вопрос по этой теме, и я помогу вам с информацией.', {"elements": null, "quick_replies": null, "buttons": null, "attachment": null, "image": null, "custom": null}, {"utter_action": "utter_architecture_response"}, 1739890189.7377212)]
2025-02-18 17:49:49 DEBUG    rasa.engine.runner.dask  - Running graph with inputs: {'__tracker__': <rasa.shared.core.trackers.DialogueStateTracker object at 0x0000024F2B4DC400>}, targets: ['select_prediction'] and ExecutionContext(model_id='1e2ff5c0db8a4015ad3ee3d512ae0e80', should_add_diagnostic_data=False, is_finetuning=False, node_name=None).
2025-02-18 17:49:49 DEBUG    rasa.engine.graph  - Node 'rule_only_data_provider' running 'RuleOnlyDataProvider.provide'.
2025-02-18 17:49:49 DEBUG    rasa.engine.graph  - Node 'domain_provider' running 'DomainProvider.provide_inference'.
2025-02-18 17:49:49 DEBUG    rasa.engine.graph  - Node 'run_MemoizationPolicy0' running 'MemoizationPolicy.predict_action_probabilities'.
2025-02-18 17:49:49 DEBUG    rasa.core.policies.memoization  - [debug    ] memoization.predict.actions    tracker_states=[{'user': {'intent': 'ask_architecture'}, 'prev_action': {'action_name': 'action_listen'}}, {'user': {'intent': 'ask_architecture'}, 'prev_action': {'action_name': 'utter_architecture_response'}}]
2025-02-18 17:49:49 DEBUG    rasa.core.policies.memoization  - There is a memorised next action 'action_listen'
2025-02-18 17:49:49 DEBUG    rasa.engine.graph  - Node 'run_RulePolicy1' running 'RulePolicy.predict_action_probabilities'.
2025-02-18 17:49:49 DEBUG    rasa.core.policies.rule_policy  - [debug    ] rule_policy.actions.find       current_states=
[state 1] user intent: ask_architecture | previous action name: action_listen
[state 2] user intent: ask_architecture | previous action name: utter_architecture_response
[state 3] user intent: ask_architecture | previous action name: action_listen
[state 4] user intent: ask_architecture | previous action name: utter_architecture_response
[state 5] user intent: ask_architecture | previous action name: action_listen
[state 6] user intent: ask_architecture | previous action name: utter_architecture_response
[state 7] user intent: ask_architecture | previous action name: action_listen
[state 8] user intent: ask_architecture | previous action name: utter_architecture_response
[state 9] user intent: ask_architecture | previous action name: action_listen
[state 10] user intent: ask_architecture | previous action name: utter_architecture_response
2025-02-18 17:49:49 DEBUG    rasa.core.policies.rule_policy  - There is a rule for the next action 'action_listen'.
2025-02-18 17:49:49 DEBUG    rasa.engine.graph  - Node 'run_TEDPolicy2' running 'TEDPolicy.predict_action_probabilities'.
2025-02-18 17:49:49 DEBUG    rasa.core.policies.ted_policy  - TED predicted 'action_listen' based on user intent.
2025-02-18 17:49:49 DEBUG    rasa.engine.graph  - Node 'select_prediction' running 'DefaultPolicyPredictionEnsemble.combine_predictions_from_kwargs'.
2025-02-18 17:49:49 DEBUG    rasa.core.policies.ensemble  - Predicted next action using RulePolicy.
2025-02-18 17:49:49 DEBUG    rasa.core.processor  - Predicted next action 'action_listen' with confidence 1.00.
2025-02-18 17:49:49 DEBUG    rasa.core.processor  - [debug    ] processor.actions.policy_prediction prediction_events=[]
2025-02-18 17:49:49 DEBUG    rasa.core.processor  - [debug    ] processor.actions.log          action_name=action_listen rasa_events=[]
2025-02-18 17:49:49 DEBUG    rasa.core.tracker_store  - No event broker configured. Skipping streaming events.
2025-02-18 17:49:49 DEBUG    rasa.core.lock_store  - Deleted lock for conversation 'PractikumStudent'.