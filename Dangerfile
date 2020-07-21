# Ensure a clean commits history
if git.commits.any? { |c| c.message =~ /^Merge branch/ }
  fail('Please rebase to get rid of the merge commits in this PR')
end

unless git.added_files.length < 5
  warn "API support, Tests, and Documentation should be added for all new features. If this MR doesn't add new features or change behavior significantly, feel free to disregard this message."
end

# Warn if too many commits
if git.commits.length >= 10
  warn "This MR adds #{git.commits.length} commits, please consider squashing this so it's smaller and easier to review."
end

# Linter
swiftlint.lint_files