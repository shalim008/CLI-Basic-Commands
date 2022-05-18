Consume Web API Post method inside ASP.NET MVC Controller

        public IActionResult Index()
        {
            var data = new LoginDto();
            data.Email = "test@gmail.com";
            data.Password = "@Pass524";
            using (var client = new HttpClient())
            {
                client.BaseAddress = new Uri("https://localhost:44352/api/Account/login");

                //HTTP POST
                var postTask = client.PostAsJsonAsync<LoginDto>("loginDto", data);
                postTask.Wait();

                var result = postTask.Result;
                if (result.IsSuccessStatusCode)
                {
                    
                }
            }

            ModelState.AddModelError(string.Empty, "Server Error. Please contact administrator.");


            return View();
        }
