int minSubsetSumDiff(vector<int>& nums) {
	size_t n{ nums.size() };
	int sum{ 0 };
	for (int i : nums) sum += i;
	vector<vector<bool>> dp(n + 1);
	for (int i = 0; i <= n; i++) {
		dp[i].resize(sum + 1);
	}
	for (int i = 0; i <= n; i++) {
		for (int j = 0; j <= sum; j++) {
			if (j == 0) {
				dp[i][j] = true;
				continue;
			}
			if (i == 0) {
				dp[i][j] = false;
				continue;
			}
			if (nums[i - 1] > j) {
				dp[i][j] = dp[i - 1][j];
				continue;
			}
			dp[i][j] = dp[i - 1][j] || dp[i - 1][j - nums[i - 1]];
		}
	}
	int subsetOne = sum / 2;
	while (!dp[n][subsetOne]) {
		--subsetOne;
	}
	return abs(sum - (2 * subsetOne));
	// (sum - closestSum) - closestSum

}
