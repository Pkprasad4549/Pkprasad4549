from github_integration import get_pull_request_data
from code_analysis import analyze_code_changes
from github_integration import post_comment_on_pull_request

def main():
    # Get pull request data
    pull_request_data = get_pull_request_data()

    # Analyze code changes
    analysis_results = analyze_code_changes(pull_request_data)

    # Generate feedback and post comments on the pull request
    post_comment_on_pull_request(pull_request_data, analysis_results)

if __name__ == '__main__':
    main()
    
