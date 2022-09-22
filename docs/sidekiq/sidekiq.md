# Sidekiq

## Sample
- Check a scheduled job

```ruby
schedule_jobs = Sidekiq::ScheduledSet.new
job_class = 'CheckTimeJob'
has_check_wave_job = false

schedule_jobs.each do |job|
  has_check_wave_job = job.item['class'] == job_class
end

p "has_check_wave_job: #{has_check_wave_job}"
```

- Check running jobs

```ruby
workers = Sidekiq::Workers.new
workers.each do |_process_id, _thread_id, work|
  p work
end
```