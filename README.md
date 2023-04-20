# Python-Project
#Selenium Project 1

#1 employee login to OrangeHRM using Python

from selenium import webdriver
from selenium.webdriver.common.keys import Keys
import time
driver = webdriver.Chrome('C:\Users\User\PycharmProjects\pythonProject\web driver')
driver.get('https://opensource-demo.orangehrmlive.com/web/index.php/auth/login')
username_field = driver.find_element_by_id('username')
username_field.send_keys('Admin')
password_field = driver.find_element_by_id('password')
password_field.send_keys('admin123')
login_button = driver.find_element_by_id('oxd-form')
login_button.click()

time.sleep(5)
driver.close()

 #2 test an invalid employee login to OrangeHRM using Python
 
from selenium import webdriver
from selenium.webdriver.common.keys import Keys
import time
 
driver = webdriver.Chrome('C:\Users\User\PycharmProjects\pythonProject\web driver')
driver.get('https://opensource-demo.orangehrmlive.com/web/index.php/auth/login')
username_field = driver.find_element_by_id('username')
username_field.send_keys('invalid_username')
password_field = driver.find_element_by_id('password')
password_field.send_keys('invalid_password')
login_button = driver.find_element_by_id('oxd-form')
login_button.click()
time.sleep(5)
error_message = driver.find_element_by_id('oxd-alert oxd-alert--error')
print(error_message.text)

driver.close()

#3 add a new employee in the PIM module in OrangeHRM using Python

from selenium import webdriver
from selenium.webdriver.common.keys import Keys
import time
driver = webdriver.Chrome('C:\Users\User\PycharmProjects\pythonProject\web driver')
driver.get('https://opensource-demo.orangehrmlive.com/web/index.php/auth/login')
username_field = driver.find_element_by_id('username')
username_field.send_keys('Admin')
password_field = driver.find_element_by_id('password')
password_field.send_keys('admin123')
login_button = driver.find_element_by_id('oxd-form')
login_button.click()
time.sleep(5)
pim_menu = driver.find_element_by_id('menu_pim_viewPimModule')
pim_menu.click()
add_employee_button = driver.find_element_by_id('oxd-button oxd-button--medium oxd-button--secondary')
add_employee_button.click()
first_name_field = driver.find_element_by_id('firstName')
first_name_field.send_keys('John')
last_name_field = driver.find_element_by_id('lastName')
last_name_field.send_keys('Doe')
employee_id_field = driver.find_element_by_id('employeeId')
employee_id_field.send_keys('1234')
save_button = driver.find_element_by_id('submit')
save_button.click()

time.sleep(5)
driver.close()

#4 edit an existing employee in the PIM module in OrangeHRM using Python

from selenium import webdriver
from selenium.webdriver.common.keys import Keys
import time
driver = webdriver.Chrome('C:\Users\User\PycharmProjects\pythonProject\web driver')
driver.get('https://opensource-demo.orangehrmlive.com/web/index.php/auth/login')
username_field = driver.find_element_by_id('username')
username_field.send_keys('Admin')
password_field = driver.find_element_by_id('password')
password_field.send_keys('admin123')
login_button = driver.find_element_by_id('oxd-form')
login_button.click()
time.sleep(5)
pim_menu = driver.find_element_by_id('menu_pim_viewPimModule')
pim_menu.click()
search_field = driver.find_element_by_id('Type for hints...')
search_field.send_keys('John Doe')
search_button = driver.find_element_by_id('submit')
search_button.click()
employee_link = driver.find_element_by_link_text('oxd-table-row oxd-table-row--with-border oxd-table-row--clickable')
employee_link.click()
edit_button = driver.find_element_by_id('oxd-icon bi-pencil-fill')
edit_button.click()
last_name_field = driver.find_element_by_id('Last Name')
last_name_field.clear()
last_name_field.send_keys('Smith')
save_button = driver.find_element_by_id('submit')
save_button.click()

time.sleep(5)
driver.close()

#5 delete an existing employee in the PIM module in OrangeHRM using Python

from selenium import webdriver
from selenium.webdriver.common.keys import Keys
import time

driver = webdriver.Chrome('C:\Users\User\PycharmProjects\pythonProject\web driver')
driver.get('https://opensource-demo.orangehrmlive.com/web/index.php/auth/login')
username_field = driver.find_element_by_id('username')
username_field.send_keys('Admin')
password_field = driver.find_element_by_id('password')
password_field.send_keys('admin123')
login_button = driver.find_element_by_id('oxd-form')
login_button.click()
time.sleep(5)
pim_menu = driver.find_element_by_id('menu_pim_viewPimModule')
pim_menu.click()
search_field = driver.find_element_by_id('oxd-autocomplete-text-input--before')
search_field.send_keys('John Doe')
search_button = driver.find_element_by_id('submit')
search_button.click()
employee_checkbox = driver.find_element_by_name('oxd-icon bi-check oxd-checkbox-input-icon')
employee_checkbox.click()
delete_button = driver.find_element_by_id('button')
delete_button.click()
confirm_button = driver.find_element_by_id('class="oxd-button oxd-button--medium oxd-button--label-danger orangehrm-button-margin"')
confirm_button.click()

time.sleep(5)
driver.close()

#Selenium Project 2

#1 search text box validation on an admin page using the python

from selenium import webdriver
from selenium.webdriver.common.keys import Keys
import time
driver = webdriver.Chrome('C:\Users\User\PycharmProjects\pythonProject\web driver')
driver.get('https://opensource-demo.orangehrmlive.com/web/index.php/auth/login')
username_field = driver.find_element_by_id('username')
username_field.send_keys('Admin')
password_field = driver.find_element_by_id('password')
password_field.send_keys('admin123')
login_button = driver.find_element_by_id('oxd-form')
login_button.click()
time.sleep(5)
search_box = driver.find_element_by_id("Search")
search_box.send_keys("oxd-main-menu-item active")
search_box.send_keys(Keys.RETURN)
results = driver.find_element_by_id("oxd-text oxd-text--span oxd-main-menu-item--name")
assert len(results) > 0
driver.quit()

#2  validation of a page header dropdown on an admin page using python

from selenium import webdriver
from selenium.webdriver.common.keys import Keys
import time

driver = webdriver.Chrome('C:\Users\User\PycharmProjects\pythonProject\web driver')
driver.get('https://opensource-demo.orangehrmlive.com/web/index.php/auth/login')
username_field = driver.find_element_by_id('username')
username_field.send_keys('Admin')
password_field = driver.find_element_by_id('password')
password_field.send_keys('admin123')
login_button = driver.find_element_by_id('oxd-form')
login_button.click()
time.sleep(5)
header_dropdown = Select(driver.find_element_by_id("oxd-topbar-body-nav-tab --parent --visited")
header_dropdown.select_by_visible_text("menuitem")
assert header_dropdown.first_selected_option.text == "user"
driver.quit()

#3 creation of new employee under the PIM (Personal Information Management) section using python

from selenium import webdriver

driver = webdriver.Chrome('C:\Users\User\PycharmProjects\pythonProject\web driver')
driver.get('https://opensource-demo.orangehrmlive.com/web/index.php/auth/login')
username_field = driver.find_element_by_id('username')
username_field.send_keys('Admin')
password_field = driver.find_element_by_id('password')
password_field.send_keys('admin123')
login_button = driver.find_element_by_id('oxd-form')
login_button.click()
pim_menu = driver.find_element_by_id('menu_pim_viewPimModule')
pim_menu.click()
add_employee_button = driver.find_element_by_id("button")
add_employee_button.click()
first_name_field = driver.find_element_by_id("firstName")
last_name_field = driver.find_element_by_id("lastName")
employee_id_field = driver.find_element_by_id("employeeId")
first_name_field.send_keys("John")
last_name_field.send_keys("Doe")
employee_id_field.send_keys("1234")
save_button = driver.find_element_by_id("submit")
save_button.click()
assert driver.current_url == "https://opensource-demo.orangehrmlive.com/web/index.php/pim/viewPersonalDetails/empNumber/1234"
driver.quit()

#4 validate an employee's personal detail page port after creating a new user using python

from selenium import webdriver

driver = webdriver.Chrome('C:\Users\User\PycharmProjects\pythonProject\web driver')
driver.get('https://opensource-demo.orangehrmlive.com/web/index.php/auth/login')
username_field = driver.find_element_by_id('username')
username_field.send_keys('Admin')
password_field = driver.find_element_by_id('password')
password_field.send_keys('admin123')
login_button = driver.find_element_by_id('oxd-form')
login_button.click()
time.sleep(5)
admin_menu = driver.find_element_by_id("oxd-main-menu-item active")
admin_menu.click()
user_management_menu = driver.find_element_by_id("oxd-topbar-body-nav-tab-item")
user_management_menu.click()
users_menu = driver.find_element_by_id("oxd-dropdown-menu")
users_menu.click()
add_user_button = driver.find_element_by_id("button")
add_user_button.click()
username_field = driver.find_element_by_id("Username")
password_field = driver.find_element_by_id("password")
confirm_password_field = driver.find_element_by_id("password")
username_field.send_keys("johndoe")
password_field.send_keys("John@123")
confirm_password_field.send_keys("John@123")
save_button = driver.find_element_by_id("submit")
save_button.click()
personal_details_tab = driver.find_element_by_id("sidenav")
personal_details_tab.click()
port_number_field = driver.find_element_by_id("personal_txtEmpNickName")
assert port_number_field.get_attribute("value") == "JD"
driver.quit()

#5 updating employe personal details page post user creation

driver = webdriver.Chrome('C:\Users\User\PycharmProjects\pythonProject\web driver')
driver.get('https://opensource-demo.orangehrmlive.com/web/index.php/auth/login')
username_field = driver.find_element_by_id('username')
username_field.send_keys('Admin')
password_field = driver.find_element_by_id('password')
password_field.send_keys('admin123')
login_button = driver.find_element_by_id('oxd-form')
login_button.click()
time.sleep(5)
admin_menu = driver.find_element_by_id("oxd-main-menu-item active")
admin_menu.click()
user_management_menu = driver.find_element_by_id("oxd-topbar-body-nav-tab-item")
user_management_menu.click()
users_menu = driver.find_element_by_id("oxd-dropdown-menu")
users_menu.click()
add_user_button = driver.find_element_by_id("button")
add_user_button.click()
username_field = driver.find_element_by_id("Username")
password_field = driver.find_element_by_id("password")
confirm_password_field = driver.find_element_by_id("password")
username_field.send_keys("johndoe")
password_field.send_keys("John@123")
confirm_password_field.send_keys("John@123")
save_button = driver.find_element_by_id("submit")
save_button.click()
personal_details_tab = driver.find_element_by_id("sidenav")
personal_details_tab.click()
edit_button = driver.find_element_by_id("btnSave")
edit_button.click()
port_number_field = driver.find_element_by_id("oxd-input oxd-input--active" data-v-844e87dc")
port_number_field.clear()
port_number_field.send_keys("doe")
save_button = driver.find_element_by_id("submit")
save_button.click()
assert port_number_field.get_attribute("value") == "doe"
driver.quit()

#6 update an employee's contact details page after creating a new user using python

from selenium import webdriver

driver = webdriver.Chrome('C:\Users\User\PycharmProjects\pythonProject\web driver')
driver.get('https://opensource-demo.orangehrmlive.com/web/index.php/auth/login')
username_field = driver.find_element_by_id('username')
username_field.send_keys('Admin')
password_field = driver.find_element_by_id('password')
password_field.send_keys('admin123')
login_button = driver.find_element_by_id('oxd-form')
login_button.click()
time.sleep(5)
admin_menu = driver.find_element_by_id("oxd-main-menu-item active")
admin_menu.click()
user_management_menu = driver.find_element_by_id("oxd-topbar-body-nav-tab-item")
user_management_menu.click()
users_menu = driver.find_element_by_id("oxd-dropdown-menu")
users_menu.click()
add_user_button = driver.find_element_by_id("button")
add_user_button.click()
username_field = driver.find_element_by_id("Username")
password_field = driver.find_element_by_id("password")
confirm_password_field = driver.find_element_by_id("password")
username_field.send_keys("johndoe")
password_field.send_keys("John@123")
confirm_password_field.send_keys("John@123")
save_button = driver.find_element_by_id("submit")
save_button.click()
contact_details_tab = driver.find_element_by_id("orangehrm-tabs-item")
contact_details_tab.click()
edit_button = driver.find_element_by_id("submit")
edit_button.click()
phone_number_field = driver.find_element_by_id("oxd-input oxd-input--active")
phone_number_field.clear()
phone_number_field.send_keys("+1-555-555-1234")
save_button = driver.find_element_by_id("submit")
save_button.click()
assert phone_number_field.get_attribute("value") == "+1-555-555-1234"
driver.quit()

#7 Updating Employe Emergency Contact number by using python

from selenium import webdriver

driver = webdriver.Chrome('C:\Users\User\PycharmProjects\pythonProject\web driver')
driver.get('https://opensource-demo.orangehrmlive.com/web/index.php/auth/login')
username_field = driver.find_element_by_id('username')
username_field.send_keys('Admin')
password_field = driver.find_element_by_id('password')
password_field.send_keys('admin123')
login_button = driver.find_element_by_id('oxd-form')
login_button.click()
time.sleep(5)
admin_menu = driver.find_element_by_id("oxd-main-menu-item active")
admin_menu.click()
user_management_menu = driver.find_element_by_id("oxd-topbar-body-nav-tab-item")
user_management_menu.click()
users_menu = driver.find_element_by_id("oxd-dropdown-menu")
users_menu.click()
add_user_button = driver.find_element_by_id("button")
add_user_button.click()
username_field = driver.find_element_by_id("Username")
password_field = driver.find_element_by_id("password")
confirm_password_field = driver.find_element_by_id("password")
username_field.send_keys("johndoe")
password_field.send_keys("John@123")
confirm_password_field.send_keys("John@123")
save_button = driver.find_element_by_id("submit")
save_button.click()
emergency_contact_tab = driver.find_element_by_id("orangehrm-tabs-item")
emergency_contact_tab.click()
add_contact_button = driver.find_element_by_id("button")
add_contact_button.click()
name_field = driver.find_element_by_id("oxd-input oxd-input--active")
relationship_field = driver.find_element_by_id("oxd-input oxd-input--active")
home_phone_field = driver.find_element_by_id("oxd-input oxd-input--active")
mobile_phone_field = driver.find_element_by_id("oxd-input oxd-input--active")
work_phone_field = driver.find_element_by_id("oxd-input oxd-input--active")
name_field.send_keys("Lily")
relationship_field.send_keys("Friend")
home_phone_field.send_keys("85469512")
mobile_phone_field.send_keys("85645752254")
work_phone_field.send_keys("789456123")
save_button = driver.find_element_by_id("submit")
save_button.click()
new_contact_name = driver.find_element_by_css_selector("#emgcontact_list tbody tr:last-child td:nth-child(2)").text
assert new_contact_name == "Lily"
driver.quit()

#8 updating employee dependent contact details page post user creation using python

from selenium import webdriver

driver = webdriver.Chrome('C:\Users\User\PycharmProjects\pythonProject\web driver')
driver.get('https://opensource-demo.orangehrmlive.com/web/index.php/auth/login')
username_field = driver.find_element_by_id('username')
username_field.send_keys('Admin')
password_field = driver.find_element_by_id('password')
password_field.send_keys('admin123')
login_button = driver.find_element_by_id('oxd-form')
login_button.click()
time.sleep(5)
admin_menu = driver.find_element_by_id("oxd-main-menu-item active")
admin_menu.click()
user_management_menu = driver.find_element_by_id("oxd-topbar-body-nav-tab-item")
user_management_menu.click()
users_menu = driver.find_element_by_id("oxd-dropdown-menu")
users_menu.click()
add_user_button = driver.find_element_by_id("button")
add_user_button.click()
username_field = driver.find_element_by_id("Username")
password_field = driver.find_element_by_id("password")
confirm_password_field = driver.find_element_by_id("password")
username_field.send_keys("johndoe")
password_field.send_keys("John@123")
confirm_password_field.send_keys("John@123")
save_button = driver.find_element_by_id("submit")
save_button.click()
dependent_tab = driver.find_element_by_id("orangehrm-tabs-item --active")
dependent_tab.click()
add_dependent_button = driver.find_element_by_id("button")
add_dependent_button.click()
name_field = driver.find_element_by_id("oxd-input oxd-input--active")
relationship_field = driver.find_element_by_id("oxd-select-text-input")
date_of_birth_field = driver.find_element_by_id("dd-mm-yyyy")
name_field.send_keys("Jane Doe")
relationship_field.send_keys("Child")
date_of_birth_field.send_keys("01/01/2000")
save_button = driver.find_element_by_id("submit")
save_button.click()
new_dependent_name = driver.find_element_by_css_selector("#dependent_list tbody tr:last-child td:nth-child(2)").text
assert new_dependent_name == "Jane Doe"
driver.quit()

#9 Updating employee job detail page using python

from selenium import webdriver

driver = webdriver.Chrome('C:\Users\User\PycharmProjects\pythonProject\web driver')
driver.get('https://opensource-demo.orangehrmlive.com/web/index.php/auth/login')
username_field = driver.find_element_by_id('username')
username_field.send_keys('Admin')
password_field = driver.find_element_by_id('password')
password_field.send_keys('admin123')
login_button = driver.find_element_by_id('oxd-form')
login_button.click()
time.sleep(5)
pim_menu = driver.find_element_by_id("oxd-main-menu-item-wrapper")
pim_menu.click()
employee_list_menu = driver.find_element_by_id("Employee List")
employee_list_menu.click()
search_field = driver.find_element_by_id("Type for hints...")
search_field.send_keys("John Smith")
search_button = driver.find_element_by_id("submit")
search_button.click()
employee_record = driver.find_element_by_xpath("//a[text()='John Smith']")
employee_record.click()
job_tab = driver.find_element_by_id("sidenav")
job_tab.find_element_by_link_text("Job").click()
job_title_field = driver.find_element_by_id("job_job_title")
job_title_field.clear()
job_title_field.send_keys("Software Engineer")
employment_status_dropdown = driver.find_element_by_id("job_emp_status")
employment_status_dropdown.click()
employment_status_dropdown.send_keys(Keys.ARROW_DOWN)
employment_status_dropdown.send_keys(Keys.RETURN)
job_category_dropdown = driver.find_element_by_id("job_eeo_category")
job_category_dropdown.click()
job_category_dropdown.send_keys(Keys.ARROW_DOWN)
job_category_dropdown.send_keys(Keys.RETURN)
save_button = driver.find_element_by_id("btnSave")
save_button.click()
driver.quit()

#10 Updating employee job detail page

from selenium import webdriver
driver = webdriver.Chrome('C:\Users\User\PycharmProjects\pythonProject\web driver')
driver.get('https://opensource-demo.orangehrmlive.com/web/index.php/auth/login')
username_field = driver.find_element_by_id('username')
username_field.send_keys('Admin')
password_field = driver.find_element_by_id('password')
password_field.send_keys('admin123')
login_button = driver.find_element_by_id('oxd-form')
login_button.click()
time.sleep(5)
pim_menu = driver.find_element_by_id("oxd-main-menu-item-wrapper")
pim_menu.click()
employee_list_menu = driver.find_element_by_id("Employee List")
employee_list_menu.click()
search_field = driver.find_element_by_id("Type for hints...")
search_field.send_keys("John Smith")
search_button = driver.find_element_by_id("submit")
search_button.click()
employee_link = driver.find_element_by_css_selector
employee_link.click()
edit_button = driver.find_element_by_id("btnSave")
edit_button.click()
job_title_field = driver.find_element_by_id("job_job_title")
job_title_field.clear()
job_title_field.send_keys("Software Engineer")
employment_status_dropdown = driver.find_element_by_id("job_emp_status")
employment_status_dropdown.click()
employment_status_dropdown.find_element_by_css_selector("option[value='1']").click()
job_category_dropdown = driver.find_element_by_id("job_eeo_category")
job_category_dropdown.click()
job_category_dropdown.find_element_by_css_selector("option[value='1']").click()
save_button = driver.find_element_by_id("btnSave")
save_button.click()
updated_job_title = driver.find_element_by_id("job_job_title").get_attribute("value")
updated_employment_status = driver.find_element_by_css_selector("#job_emp_status option[selected='selected']").text
updated_job_category = driver.find_element_by_css_selector("#job_eeo_category option[selected='selected']").text
assert updated_job_title == "Software Engineer"
assert updated_employment_status == "Full-Time Permanent"
assert updated_job_category == "Technical"
driver.quit()

#11 Updating employee job activation on job details page using python

from selenium import webdriver

driver = webdriver.Chrome('C:\Users\User\PycharmProjects\pythonProject\web driver')
driver.get('https://opensource-demo.orangehrmlive.com/web/index.php/auth/login')
username_field = driver.find_element_by_id('username')
username_field.send_keys('Admin')
password_field = driver.find_element_by_id('password')
password_field.send_keys('admin123')
login_button = driver.find_element_by_id('oxd-form')
login_button.click()
time.sleep(5)
pim_menu = driver.find_element_by_id("oxd-main-menu-item-wrapper")
pim_menu.click()
employee_list_menu = driver.find_element_by_id("Employee List")
employee_list_menu.click()
search_field = driver.find_element_by_id("Type for hints...")
search_field.send_keys("John Smith")
search_button = driver.find_element_by_id("submit")
search_button.click()
employee_link = driver.find_element_by_css_selector
employee_link.click()
edit_button = driver.find_element_by_id("btnSave")
edit_button.click()
job_status_checkbox = driver.find_element_by_id("job_is_active")
job_status_checkbox.click()
save_button = driver.find_element_by_id("btnSave")
save_button.click()
updated_job_status = driver.find_element_by_id("job_is_active").is_selected()
assert updated_job_status == True
driver.quit()

#12 updating employee salary componant page using python

from selenium import webdriver
from selenium.webdriver.common.keys import Keys

driver = webdriver.Chrome('C:\Users\User\PycharmProjects\pythonProject\web driver')
driver.get('https://opensource-demo.orangehrmlive.com/web/index.php/auth/login')
username_field = driver.find_element_by_id('username')
username_field.send_keys('Admin')
password_field = driver.find_element_by_id('password')
password_field.send_keys('admin123')
login_button = driver.find_element_by_id('oxd-form')
login_button.click()
time.sleep(5)
pim_menu = driver.find_element_by_id("oxd-main-menu-item-wrapper")
pim_menu.click()
employee_list_menu = driver.find_element_by_id("Employee List")
employee_list_menu.click()
search_field = driver.find_element_by_id("Type for hints...")
search_field.send_keys("John Smith")
search_button = driver.find_element_by_id("submit")
search_button.click()
employee_link = driver.find_element_by_css_selector
employee_link.click()
salary_tab = driver.find_element_by_id("sidenav")
salary_tab.find_element_by_link_text("Salary").click()
basic_salary = driver.find_element_by_id("salary_salary_component_1_salary")
basic_salary.clear()
basic_salary.send_keys("5000")
save_button = driver.find_element_by_id("btnSave")
save_button.click()
welcome_menu = driver.find_element_by_id("welcome")
welcome_menu.click()
logout_button = driver.find_element_by_link_text("Logout")
logout_button.click()
driver.quit()

#13 Updating employee salary on tax exemption page

from selenium import webdriver
from selenium.webdriver.common.keys import Keys
driver = webdriver.Chrome('C:\Users\User\PycharmProjects\pythonProject\web driver')
driver.get('https://opensource-demo.orangehrmlive.com/web/index.php/auth/login')
username_field = driver.find_element_by_id('username')
username_field.send_keys('Admin')
password_field = driver.find_element_by_id('password')
password_field.send_keys('admin123')
login_button = driver.find_element_by_id('oxd-form')
login_button.click()
time.sleep(5)
pim_menu = driver.find_element_by_id("oxd-main-menu-item-wrapper")
pim_menu.click()
employee_list_menu = driver.find_element_by_id("Employee List")
employee_list_menu.click()
search_field = driver.find_element_by_id("Type for hints...")
search_field.send_keys("John Smith")
search_button = driver.find_element_by_id("submit")
search_button.click()
employee_link = driver.find_element_by_css_selector
employee_link.click()
tax_link = driver.find_element_by_id("sidenav")
tax_link.find_element_by_link_text("Tax Exemptions").click()
salary_field = driver.find_element_by_id("tax_exempt_amount")
salary_field.clear()
salary_field.send_keys("5000")
driver.find_element_by_id("btnSave").click()
driver.quit()
