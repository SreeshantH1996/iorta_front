<template>
  <div>
    <div class="cont">
      <div style="margin: 7%; text-align: left; margin-bottom: 13%">
        <h4>Please verify the detials and upload the required documents.</h4>
        <div style="margin-top: 2%">
          <div class="row">
            <div class="col-6">
              <b>District : {{UserDetials.district}}</b>
            </div>
            <div class="col-6">
              <b>Phone Number : {{UserDetials.phnumber}}</b>
            </div>
          </div>

          <div class="row">
            <div class="col-6">
              <b>Name of Applicant : {{UserDetials.name}}</b>
            </div>
            <div class="col-6">
              <b>Realtion : {{UserDetials.relation_with}} , Name : {{UserDetials.relation_name}}</b>
            </div>
          </div>

          <div class="row">
            <div class="col-6">
              <b>Gender : {{UserDetials.gender}}</b>
            </div>
            <div class="col-6">
              <b>Qualification : {{UserDetials.qualification}}</b>
            </div>
          </div>

          <div class="row">
            <div class="col-6">
              <b>Emergency Phone Number : {{UserDetials.emphnumber}}</b>
            </div>
            <div class="col-6">
              <b>Date Of birth : {{UserDetials.dob}}</b>
            </div>
          </div>

          <div class="row">
            <div class="col-6">
              <b>Country Of Birth : {{UserDetials.country}}</b>
            </div>
            <div class="col-6">
              <b>Blood Group : {{UserDetials.blood}}</b>
            </div>
          </div>

          <div class="row">
            <div class="col-6">
              <b
                >Identification Mark 1 :
                {{UserDetials.identificationmark1}}</b
              >
            </div>
            <div class="col-6">
              <b>Identification Mark 2 : {{UserDetials.identificationmark2}}</b>
            </div>
          </div>

          <hr />
          <h4>Permanent Address</h4>
          <div class="row">
            <div class="col-6">
              <b>House Name / Number : {{UserDetials.prhousename}}</b>
            </div>
            <div class="col-6">
              <b>Street : {{UserDetials.prstreet}}</b>
            </div>
          </div>

          <div class="row">
            <div class="col-6">
              <b>Location : {{UserDetials.prlocation}}</b>
            </div>
            <div class="col-6">
              <b>Pincode : {{UserDetials.prpincode}}</b>
            </div>
          </div>

          <div class="row">
            <div class="col-6">
              <b>Village : {{UserDetials.prvillage}}</b>
            </div>
            <div class="col-6">
              <b>Taluk : {{UserDetials.prtaluk}}</b>
            </div>
          </div>

          <hr />
          <h4>Temperory Address</h4>
          <div class="row">
            <div class="col-6">
              <b>House Name / Number : {{UserDetials.trhousename}}</b>
            </div>
            <div class="col-6">
              <b>Street : {{UserDetials.tstreet}}</b>
            </div>
          </div>

          <div class="row">
            <div class="col-6">
              <b>Location : {{UserDetials.trlocation}}</b>
            </div>
            <div class="col-6">
              <b>Pincode : {{UserDetials.trpincode}}</b>
            </div>
          </div>

          <div class="row">
            <div class="col-6">
              <b>Village : {{UserDetials.trvillage}}</b>
            </div>
            <div class="col-6">
              <b>Taluk : {{UserDetials.trtaluk}}</b>
            </div>
          </div>
        </div>
        <div class="row" style="margin-top: 4%">
          <div class="col-12">
            <a href="/#/createlicence/">
              <button class="btn btn-lg btn-primary">Edit Details</button>
            </a>
          </div>
        </div>
        <hr />
        <div style="margin-top: 2%">
          <h4>Upload Documnets</h4>
          <form v-on:submit.prevent="UploadDocuments()" id="uploaddocuments">
            <div class="row" style="margin-top: 3%">
              <div class="col-6">
                <div class="form-group">
                  <select name="identity_type" class="form-control" required>
                    <option value="" >Select ID proof</option>
                    <option value="sslc">SSLC Certificate</option>
                    <option value="adhar">Adhar</option>
                    <option value="vid">Voter ID</option>
                    <option value="passport">Passport</option>
                  </select>
                </div>
              </div>
              <div class="col-6">
                <div class="form-group">

                  <input
                    type="file"
                    class="form-control-file"
                    accept="application/pdf"
                    name="identityproof"
                    required
                  />
                  <span v-if="UserDocuments.identitycertificate">
                   <i>Current document : <a v-bind:href="'http://localhost:8000'+ UserDocuments.identitycertificate" target="__blank">click here</a></i>
                  </span>
                </div>
              </div>
            </div>
            <div class="row">
              <div class="col-6">
                <div class="form-group">
                  <label
                    >Eye Certificate<span style="color: red">*</span></label
                  >
                </div>
              </div>
              <div class="col-6">
                <div class="form-group">
 
                  <input
                    type="file"
                    class="form-control-file"
                    accept="application/pdf"
                    name="eyecertificate"
                    required
                  />
                  <span v-if="UserDocuments.eyecertificate">
                   <i>Current document : <a v-bind:href="'http://localhost:8000'+ UserDocuments.eyecertificate" target="__blank">click here</a></i>
                  </span>
                </div>
              </div>
            </div>
            <div class="row">
              <div class="col-6">
                <div class="form-group">
                  <label
                    >Self Declaration Form
                    <span style="color: red">*</span></label
                  >
                </div>
              </div>
              <div class="col-6">
                <div class="form-group">

                  <input
                    type="file"
                    class="form-control-file"
                    accept="application/pdf"
                    name="selfdeclarationfrom"
                    required
                  />
                  <span v-if="UserDocuments.selfcertificate">
                   <i>Current document : <a v-bind:href="'http://localhost:8000'+ UserDocuments.selfcertificate" target="__blank">click here</a></i>
                  </span>
                </div>
              </div>
            </div>
            <div class="row">
              <div class="col-6">
                <div class="form-group">
                  <label
                    >Photo of Applicant<span style="color: red">*</span></label
                  >
                </div>
              </div>
              <div class="col-6">
                <div class="form-group">

                  <input
                    type="file"
                    class="form-control-file"
                    accept=".jpg,.gif,.png"
                    name="photo"
                    required
                  />
                  <span v-if="UserDocuments.photo">
                   <i>Current document : <a v-bind:href="'http://localhost:8000'+ UserDocuments.photo" target="__blank">click here</a></i>
                  </span>
                </div>
              </div>
            </div>
            <div class="row">
              <div class="col-6">
                <div class="form-group">
                  <label>Signature<span style="color: red">*</span></label>
                </div>
              </div>
              <div class="col-6">
                <div class="form-group">

                  <input
                    type="file"
                    class="form-control-file"
                    accept=".jpg,.gif,.png"
                    name="signature"
                    required
                  />
                  <span v-if="UserDocuments.signature">
                   <i>Current document : <a v-bind:href="'http://localhost:8000'+ UserDocuments.signature" target="__blank">click here</a></i>
                  </span>
                </div>
              </div>
            </div>

            <span style="color: red">All fields with * mark is mandatory</span>
            <div class="row" style="margin-top: 2%; margin-bottom: 2%">
              <div class="col-6">
                <button type="submit" class="btn btn-lg btn-primary">
                  Submit
                </button>
              </div>
              <div class="col-6" style="text-align: right">
                <a href="/#/userhome">
                  <button type="button" class="btn btn-lg btn-primary">
                    Cancel
                  </button>
                </a>
              </div>
            </div>
          </form>
        </div>
      </div>
      <!-- <div>
          <button id="rzp-button1" v-on:click="payMoney()">Pay</button>
      </div> -->
    </div>
  </div>
</template>    
<script lang="ts" src="../ts/UploadDocuments.ts"></script>
<style scoped src="../css/UploadDocuments.css"></style>