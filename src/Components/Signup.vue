<template>
    <div id="signupbox" style="margin-top:50px"
         class="mainbox col-md-6 col-md-offset-3 col-sm-8 col-sm-offset-2">
        <div class="panel panel-info">
            <div class="panel-heading">
                <div class="panel-title">Sign Up</div>
                <div style="float:right; font-size: 85%; position: relative; top:-10px"><a href="#" id="signinlink" @click="signinButtonAction">Sign In</a>
                </div>
            </div>
            <div class="panel-body">
                <form id="signupform" class="form-horizontal" role="form">

                    <div id="signupalert" style="display:none" class="alert alert-danger">
                        <p>Error:</p>
                        <span></span>
                    </div>
                    <div class="form-group">
                        <label for="username-Field" class="col-md-3 control-label">Username</label>
                        <div class="col-md-9">
                            <input type="text" class="form-control" name="username" placeholder="Username"
                                   id="username-Field">
                        </div>
                    </div>
                    <div class="form-group">
                        <label for="name-Field" class="col-md-3 control-label">Name</label>
                        <div class="col-md-9">
                            <input type="text" class="form-control" name="name" placeholder="Name" id="name-Field">
                        </div>
                    </div>
                    <div class="form-group">
                        <label for="password-Field" class="col-md-3 control-label">Password</label>
                        <div class="col-md-9">
                            <input type="password" class="form-control" name="passwd" placeholder="Password"
                                   id="password-Field">
                        </div>
                    </div>
                    <div class="form-group">
                        <label for="icode-Field" class="col-md-3 control-label">Invitation Code</label>
                        <div class="col-md-9">
                            <input type="text" class="form-control" name="icode" placeholder="" id="icode-Field">
                        </div>
                    </div>
                    <div class="form-group">
                        <!-- Button -->
                        <div class="col-md-offset-3 col-md-9">
                            <button id="btn-signup" type="button" class="btn btn-info"><i
                                    class="icon-hand-right"></i> &nbsp; Sign Up
                            </button>
                            <span style="margin-left:8px;">or</span>
                        </div>
                    </div>
                    <div style="border-top: 1px solid #999; padding-top:20px" class="form-group">
                        <div class="col-md-offset-3 col-md-9">
                            <button id="btn-fbsignup" type="button" class="btn btn-primary"><i
                                    class="icon-facebook"></i> Sign Up with Github
                            </button>
                        </div>
                    </div>
                </form>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        props:['signinButtonAction']
    }
</script>
