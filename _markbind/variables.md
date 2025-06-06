<!-- ===========================  primary course configuration ============================================= -->

<variable name="course">CS2103</variable>
<variable name="course_pair">{{ course }}/T</variable>
<variable name="course_name">Software Engineering</variable>
<variable name="course_color">success</variable>

<variable name="S">1</variable>
<variable name="semester">AY2021S{{ S }}</variable>
<variable name="period">2020 Aug-Dec</variable>
<variable name="current_week">-1</variable>

<variable name="algolia">no</variable>

<variable name="canvas_course_id">36678</variable>
<variable name="url_instructors">https://docs.google.com/document/d/e/2PACX-1vQe3k_8EDv73v8PmGf0vjoJWVh1eixYQ31_sNHz1eKfRjVciSwZJ9UDu6H1H4ZxVmqKy9CY4vRAq7cv/pub?embedded=true</variable>
<variable name="url_coursemology_classroom">https://coursemology.org/courses/2020</variable>
<variable name="url_ms_teams_class">x</variable>

<variable name="date_w1_start">2022-01-10</variable>
<variable name="day_first_tutorial">Wednesday</variable>
<variable name="recess_after_week">6</variable>
<variable name="lecture_venue">LT15</variable>
<variable name="time_lecture_start">1600</variable>
<variable name="time_lecture_end">1800</variable>
<variable name="time_t_lecture_start">1600</variable>
<variable name="time_t_lecture_end">1800</variable>
<variable name="ped_week">11</variable>
<variable name="pe_week">12</variable>
<variable name="show_feature_freeze_dashboards">yes</variable>
<variable name="catcher_load_testing"></variable> <!-- keep empty if load testing falls on a holiday -->

<variable name="ip_name">iP</variable>
<variable name="ip_repo_name">ip</variable>
<variable name="ip_first_week">2</variable>
<variable name="ip_last_week">8</variable>

<variable name="tp_first_week">3</variable>
<variable name="version_practice">v1.1</variable>
<variable name="version_first">v1.2</variable>
<variable name="version_mvp">v1.3</variable>
<variable name="version_alpha">v1.4</variable>
<variable name="version_penultimate">v1.5</variable>
<variable name="version_final">v1.6</variable>
<variable name="version_future">v2.0</variable>
<variable name="example_team_id">{{ course }}-T09-2</variable>
<variable name="tp_pe_bug_count">6</variable>

<variable name="ug_pages_per_person">1</variable>
<variable name="dg_pages_per_person">3</variable>
<variable name="uml_diagrams_per_person">2 types of</variable>

<variable name="marks_ip">30</variable>
<variable name="marks_ip_implementation">15</variable>
<variable name="marks_ip_pm">10</variable>
<variable name="marks_ip_documentation">5</variable>
<variable name="marks_tp">45</variable>
<variable name="marks_tp_design">5</variable>
<variable name="marks_tp_documentation">10</variable>
<variable name="marks_tp_implementation">10</variable>
<variable name="marks_tp_pm">10</variable>
<variable name="marks_tp_pm_individual">5</variable>
<variable name="marks_tp_pm_team">5</variable>
<variable name="marks_tp_qa">10</variable>
<variable name="marks_tp_individual">35</variable>
<variable name="marks_tp_team">10</variable>
<variable name="marks_participation">5</variable>
<variable name="marks_exam">30</variable>
<variable name="marks_exam_essay">0</variable>
<variable name="marks_exam_mcq">30</variable>
<variable name="marks_ca">70</variable>
<variable name="mcq_count">100</variable>

<variable name="lecture_name_upper">Lecture</variable>
<variable name="lecture_name">{{ lecture_name_upper | lower }}</variable>
<variable name="lecture_name_short">{{ lecture_name }}</variable>

<variable name="pe_seat_numbers_gsheet">https://docs.google.com/spreadsheets/d/e/2PACX-1vSUbcJpMC5OdJkr_K6VxDwAkkrwJsqAFSPwHmZq88EbOdAWIPMeYvDQDYOUEcsEYVwACmAz5hH0W0ZY/pubhtml?gid=0&single=true</variable>

<!-- ===========================  secondary variables =========================================== -->

<variable name="cs2103">{{ "Y" if course == "CS2103" }}</variable>
<variable name="cs2113">{{ "Y" if course == "CS2113" }}</variable>
<variable name="tic2002">{{ "Y" if course == "TIC2002" }}</variable>
<variable name="tee3201">{{ "Y" if course == "TEE3201" }}</variable>
<variable name="has_t">{{ "Y" if cs2103 }}</variable>
<variable name="has_pe">{{ "Y" if cs2103 or cs2113 }}</variable>
<variable name="session_name">tutorial</variable>
<variable name="Session_name">Tutorial</variable>

<variable name="tp_repo_name">tp</variable>

<variable name="pe_schedule_ideal">{{ "yes" if (ped_week == "11" and pe_week == "12") else "" }}</variable>
<variable name="pe_schedule_late">{{ "yes" if (ped_week == "12" and pe_week == "13") else "" }}</variable>
<variable name="pe_schedule_stretched">{{ "yes" if (ped_week == "11" and pe_week == "13") else "" }}</variable>

<variable name="w6_days">{{ 14 if recess_after_week == "6" else 7 }}</variable>
<variable name="w7_days">{{ 14 if recess_after_week == "7" else 7 }}</variable>

<variable name="format_normal">ddd, MMM Do</variable>
<variable name="format_full_day">dddd</variable>
<variable name="date_first_lecture">{{ date_w1_start | date("YYYY-MM-DD", 4) }}</variable>
<variable name="day_lecture">{{ date_first_lecture | date(format_full_day) }}</variable>
<variable name="date_final_submission">{{ date_w1_start | date("YYYY-MM-DD", 92 if pe_schedule_late else 85) }}</variable>
<variable name="time_final_submission">14:00</variable>
<variable name="date_w2_start">{{ date_w1_start | date("YYYY-MM-DD", 7) }}</variable>
<variable name="date_w3_start">{{ date_w2_start | date("YYYY-MM-DD", 7) }}</variable>
<variable name="date_w4_start">{{ date_w3_start | date("YYYY-MM-DD", 7) }}</variable>
<variable name="date_w5_start">{{ date_w4_start | date("YYYY-MM-DD", 7) }}</variable>
<variable name="date_w6_start">{{ date_w5_start | date("YYYY-MM-DD", 7) }}</variable>
<variable name="date_w7_start">{{ date_w6_start | date("YYYY-MM-DD", (w6_days | int)) }}</variable>
<variable name="date_w8_start">{{ date_w7_start | date("YYYY-MM-DD", (w7_days | int)) }}</variable>
<variable name="date_w9_start">{{ date_w8_start | date("YYYY-MM-DD", 7) }}</variable>
<variable name="date_w10_start">{{ date_w9_start | date("YYYY-MM-DD", 7) }}</variable>
<variable name="date_w11_start">{{ date_w10_start | date("YYYY-MM-DD", 7) }}</variable>
<variable name="date_w12_start">{{ date_w11_start | date("YYYY-MM-DD", 7) }}</variable>
<variable name="date_w13_start">{{ date_w12_start | date("YYYY-MM-DD", 7) }}</variable>
<variable name="date_w14_start">{{ date_w13_start | date("YYYY-MM-DD", 7) }}</variable>

<variable name="course_email">{{ course | lower }}@comp.nus.edu.sg</variable>
<variable name="course_org">nus-{{ course | lower }}-{{ period if tic2002 or tee3201 else semester }}</variable>
<variable name="url_course_org">https://github.com/{{ course_org }}</variable>
<variable name="url_course_gihub_io">https://{{ course_org | lower }}.github.io</variable>

<variable name="url_admin"><md>[Admin Info page]({{baseUrl}}/admin/index.html)</md></variable>
<variable name="url_announcements">https://canvas.nus.edu.sg/courses/{{ canvas_course_id }}/announcements</variable>
<variable name="url_bugs">{{ url_course_org | safe }}/forum/issues</variable>
<variable name="url_canvas_home">https://canvas.nus.edu.sg/courses/{{ canvas_course_id }}</variable>
<variable name="url_dashboards">{{ url_course_gihub_io | safe }}/dashboards</variable>
<variable name="url_files">https://canvas.nus.edu.sg/courses/{{ canvas_course_id }}/files</variable>
<variable name="url_forum">{{ url_course_org | safe }}/forum/issues</variable>
<variable name="link_forum">[course forum]({{ url_forum }})</variable>
<variable name="url_forum_activities_dashboard">{{ url_dashboards }}/contents/forum-activities.html</variable>
<variable name="url_ab3_fork_website">{{ url_course_gihub_io | safe }}/{{ tp_repo_name }}</variable>
<variable name="url_ab3_upstream_website">https://se-education.org/addressbook-level3</variable>
<variable name="url_java_coding_standard">https://se-education.org/guides/conventions/java/{{ "intermediate" if cs2103 else "basic"}}.html</variable>
<variable name="url_git_conventions">https://se-education.org/guides/conventions/git.html</variable>
<variable name="url_ip_dashboard">{{ url_course_gihub_io | safe }}/ip-dashboard/?search=&sort=groupTitle&sortWithin=title&timeframe=commit&mergegroup=&groupSelect=groupByRepos&breakdown=true&checkedFileTypes=java~md~fxml~sh~bat~gradle~txt</variable>
<variable name="url_ip_progress_dashboard">{{ url_dashboards }}/contents/ip-progress.html</variable>
<variable name="url_course_website">{{ url_course_gihub_io | safe }}/website</variable>
<variable name="url_participation_dashboard">{{ url_dashboards }}/contents/participation.html</variable>
<variable name="url_quizzes">https://canvas.nus.edu.sg/courses/{{ canvas_course_id }}/quizzes</variable>
<variable name="url_schedule"><md>[Weekly Schedule Page]({{baseUrl}}/schedule/index.html)</md></variable>
<variable name="url_team_list">{{baseUrl}}/admin/teamList.html</variable>
<variable name="url_tp_dashboard_base">{{ url_course_gihub_io | safe }}/tp-dashboard/?search=&sort=groupTitle&sortWithin=title&timeframe=commit&mergegroup=&groupSelect=groupByRepos&breakdown=true</variable>
<variable name="url_tp_dashboard">{{ url_tp_dashboard_base }}&checkedFileTypes=docs~functional-code~test-code~other</variable>
<variable name="url_tp_dashboard_fc_only">{{ url_tp_dashboard_base }}&checkedFileTypes=functional-code</variable>
<variable name="url_tp_feature_freeze_dashboard">{{ url_tp_dashboard_fc_only | replace ("/tp-dashboard/", "/tp-feature-freeze-dashboard/") }}</variable>
<variable name="url_tp_progress_dashboard">{{ url_dashboards }}/contents/tp-progress.html</variable>

<!-- ===========================  icons ================================================= -->

<variable id="bullet_checkbox">{ icon="far-square" }</variable>
<variable id="bullet_checkbox_red">{ icon="far-square" i-class="text-danger" }</variable>
<variable id="bullet_checkbox_selected">{ icon="fas-square-check" }</variable>
<variable id="bullet_checkbox_selected_green">{ icon="fas-square-check" i-class="text-success" }</variable>
<variable id="bullet_important_red">{ icon="fas-circle-exclamation" i-class="text-danger" }</variable>
<variable id="bullet_info">{ icon="fas-info-circle" i-class="text-info" }</variable>
<variable id="bullet_Q">{ icon="glyphicon-question-sign" i-class="text-info" }</variable>
<variable id="bullet_target_green">{ icon="fas-crosshairs" i-class="text-success" }</variable>
<variable id="bullet_tick_green">{ icon="fas-check" i-class="text-success" }</variable>
<variable id="bullet_tip">{ icon="fas-lightbulb" i-class="badge rounded-pill bg-success text-white my-1" i-size="10px" }</variable>
<variable id="bullet_x_red">{ icon="fas-times" i-class="text-danger" }</variable>

<variable name="icon_alert"><span class="badge rounded-pill bg-danger text-light">:fas-exclamation: ALERT</span></variable>
<variable name="icon_announcement"><md>:fas-bell:</md></variable>
<variable name="icon_book"><md>:fas-book:</md></variable>
<variable name="icon_calendar"><md>:fas-calendar-alt:</md></variable>
<variable name="icon_deadline"><md>:far-clock:</md></variable>
<variable name="icon_dislike"><md>:fas-thumbs-down:</md></variable>
<variable name="icon_example"><md>:fas-cube:</md></variable>
<variable name="icon_embedding"><md>:glyphicon-log-in:</md></variable>
<variable name="icon_exercise"><md>:fas-dumbbell:</md></variable>
<variable name="icon_extra"><span class='badge rounded-pill bg-secondary'><md>:fas-plus: extra</md></span></variable>
<variable name="icon_evidence"><md>:fas-briefcase:</md></variable>
<variable name="icon_graded"><span class="text-info"><tooltip content="counted for participation"><md>:fab-product-hunt:</md></tooltip></span></variable>
<variable name="icon_info"><md>:fas-info-circle:</md></variable>
<variable name="icon_lecture"><md>:glyphicon-blackboard:</md></variable>
<variable name="icon_like"><md>:fas-thumbs-up:</md></variable>
<variable name="icon_linux"><md>:fab-linux:</md></variable>
<variable name="icon_important_big_red"><span style="color: red">++<md>:glyphicon-exclamation-sign:</md>++</span></variable>
<variable name="icon_important"><md>:glyphicon-exclamation-sign:</md></variable>
<variable name="icon_new_window"><md>:glyphicon-new-window:</md></variable>
<variable name="icon_outcome"><md>:fas-trophy:</md></variable>
<variable name="icon_output"><md>:fas-arrow-down:</md></variable>
<variable name="icon_output_right"><md>:fas-arrow-right:</md></variable>
<variable name="icon_pr"><md>:octicon-git-pull-request:</md></variable>
<variable name="icon_prereq"><md>:glyphicon-education:</md></variable>
<variable name="icon_preview"><md>:glyphicon-eye-open:</md></variable>
<variable name="icon_print"><md>:glyphicon-print:</md></variable>
<variable name="icon_pro_tip"><span class="badge rounded-pill bg-success text-light">:fas-lightbulb: PRO TIP</span></variable>
<variable name="icon_project"><md>:fas-drafting-compass:</md></variable>
<variable name="icon_Q"><md>:glyphicon-question-sign:</md></variable>
<variable name="icon_green_Q"><thumbnail circle text="**Q**" background="#28a745" font-color="white" size="25"/></variable>
<variable name="icon_Q_A">{{ icon_Q | safe }}:glyphicon-ok-sign:</variable>
<variable name="icon_repo"><md>:fas-code-branch:</md></variable>
<variable name="icon_resource"><md>:fas-paperclip:</md></variable>
<variable name="icon_terminal"><small><span class="badge bg-secondary">&gt;_</span></small></variable>
<variable name="icon_text"><md>:far-file-alt:</md></variable>
<variable name="icon_tick"><md>:fas-check:</md></variable>
<variable name="icon_tip"><span class="badge rounded-pill bg-success text-white">:fas-lightbulb:</span></variable>
<variable name="icon_tick_green"><span style="color: green">{{ icon_tick | safe }}</span></variable>
<variable name="icon_todo"><md>:glyphicon-check:</md></variable>
<variable name="icon_try">:fas-laptop:</variable>
<variable name="icon_tutorial"><md>:fas-chalkboard-teacher:</md></variable>
<variable name="icon_slides"><md>:far-images:</md></variable>
<variable name="icon_video"><md>:glyphicon-facetime-video:</md></variable>
<variable name="icon_warning"><span class="badge rounded-pill bg-warning text-dark">:fas-exclamation:</span></variable>
<variable name="icon_windows"><md>:fab-windows:</md></variable>
<variable name="icon_x"><md>:fas-times:</md></variable>
<variable name="icon_x_red"><span style="color: red">{{ icon_x | safe }}</span></variable>

<variable name="icon_tab_admin_info">{{ icon_info | safe }}</variable>
<variable name="icon_tab_project">{{ icon_project | safe }}</variable>
<variable name="icon_tab_programming_topics"><md>:fas-code:</md></variable>
<variable name="icon_tab_tasks">{{ icon_todo | safe }}</variable>
<variable name="icon_tab_topics">{{ icon_book | safe }}</variable>
<variable name="icon_tab_tutorial">{{ icon_tutorial | safe }}</variable>
<variable name="icon_tab_summary">{{ icon_announcement | safe }}</variable>

<variable name="icon_individual"><md>:fas-user:</md></variable>
<variable name="icon_team"><md>:fas-users:</md></variable>
<variable id="icon_team_rep"><md>:fas-user:%%/:fas-users:%%</md></variable>
<variable name="icon_both">{{ icon_individual }}/{{ icon_team }}</variable>

<variable name="faq"><span class="badge rounded-pill bg-info"><md>:far-question: FAQ</md></span></variable>
<variable name="bad"><span style="color: red"><md>:fas-thumbs-down: Bad</md></span></variable>
<variable name="good"><span style="color: green"><md>:fas-thumbs-up: Good</md></span></variable>
<variable name="pros"><span class="text-success">:fas-thumbs-up: pros:</span></variable>
<variable name="cons"><span class="text-danger">:fas-thumbs-down: cons:</span></variable>
<variable name="conditional"><span class="badge rounded-pill bg-warning text-dark">CONDITIONAL</span></variable>
<variable name="required"><span class="badge rounded-pill bg-danger">REQUIRED</span></variable>
<variable name="optional"><span class="badge rounded-pill bg-success">OPTIONAL</span></variable>
<variable name="evidence">++{{ icon_evidence | safe }} Evidence:++</variable>

<variable name="edition_badge"><small><small><small><span class='badge rounded-pill bg-{{ course_color }}'>{{ course_pair }} edition - {{ period }}</span></small></small></small></variable>
<variable name="M"><span class="badge bg-info">&nbsp;{{ course }}&nbsp;</span></variable>
<variable name="MT"><span class="badge bg-warning text-dark">{{ course }}T</span></variable>

<variable name="heading_project"><h3 class="bg-dark text-white p-2 mb-4 mt-4">{{ icon_project }} Project</h3></variable>

<variable name="s"><md>:glyphicon-flash:</md></variable>
<variable name="star"><span class='glyphicon glyphicon-flash' aria-hidden='true'></span></variable>
<variable name="one_star"><span class='badge rounded-pill bg-light text-danger'>{{ star | safe }} </span></variable>
<variable name="prereq_no_stars"><span class='badge rounded-pill bg-secondary'>{{ icon_prereq | safe }}{{ icon_prereq | safe }}</span></variable>
<variable name="prereq_one_star"><span class='badge rounded-pill bg-secondary'>{{ icon_prereq | safe }}{{ icon_prereq | safe }} : {{ star | safe }} </span></variable>
<variable name="two_stars"><span class='badge rounded-pill bg-light text-warning'>{{ star | safe }}{{ star | safe }} </span></variable>
<variable name="prereq_two_stars"><span class='badge rounded-pill bg-secondary'>{{ icon_prereq | safe }}{{ icon_prereq | safe }} : {{ star | safe }}{{ star | safe }} </span></variable>
<variable name="three_stars"><span class='badge rounded-pill bg-light text-primary'>{{ star | safe }}{{ star | safe }}{{ star | safe }} </span></variable>
<variable name="prereq_three_stars"><span class='badge rounded-pill bg-secondary'>{{ icon_prereq | safe }}{{ icon_prereq | safe }} : {{ star | safe }}{{ star | safe }}{{ star | safe }} </span></variable>
<variable name="four_stars"><span class='badge rounded-pill bg-success'>{{ star | safe }}{{ star | safe }}{{ star | safe }}{{ star | safe }}: OPTIONAL</span></variable>
<variable name="prereq_four_stars"><span class='badge rounded-pill bg-secondary'>{{ icon_prereq | safe }}{{ icon_prereq | safe }} : {{ star | safe }}{{ star | safe }}{{ star | safe }}{{ star | safe }} </span></variable>

<!-- ===========================  misc aliases =========================================== -->

<variable name="line_dashed"><hr style="border-top: dashed 1px; border-color:grey" /></variable>
<variable name="line_dotted"><hr style="border-width: 1px; border-color: #f3ccff; border-style: dotted"></variable>
<variable name="line_double"><hr style="border-top: 3px double #c5c5c5;"></variable>
<variable name="pagebreak"><p style="page-break-after: always;">&nbsp;</p></variable>
<variable id="lecture_table_headers">
Course                 | Venue    | Time
---------------------- | -------- | ----
</variable>
<variable id="tutorial_table_headers">
Course | Venue | Time | ~~%%Tutorial ID<br>in Canvas%%~~<br>==(don't use this!)== | **Our Tutorial ID**<br>==(use this!)== | Tutor<br>of teams 1,2 | Tutor<br>of teams 3,4
-------|-------|------|------------------------------------------------------------|----------------------------------------|-------|----
</variable>
