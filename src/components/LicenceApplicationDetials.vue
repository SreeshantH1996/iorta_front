<template>
  <div>
    <div class="cont">
      <div style="margin: 7%; text-align: left; margin-bottom: 13%">
        <h4><b>Application Details</b></h4>
        <div style=" padding 2%;">
          <div class="row">
            <div class="col-9" style="text-align: left">
              <b
                ><img
                  style="width: 40%; margin-bottom: 2%; margin-top: 2%"
                  :src="'http://localhost:8000' + document_list.photo"
                  class="img-rounded"
                  alt="Cinque Terre"
              /></b>
            </div>
          </div>
          <div class="row">
            <div class="col-2">Applicant Name</div>
            <div class="col-1">:</div>
            <div class="col-9">
              <b>{{ application_details.name }}</b>
            </div>
            
          </div>
          <div class="row">
            <div class="col-2">District</div>
            <div class="col-1">:</div>
            <div class="col-9">
              <b>{{ application_details.district }}</b>
            </div>
          </div>
          <div class="row">
            <div class="col-2">DOB</div>
            <div class="col-1">:</div>
            <div class="col-9">
              <b>{{ application_details.dob }}</b>
            </div>
          </div>
          <div class="row">
            <div class="col-2">Phone Numer</div>
            <div class="col-1">:</div>
            <div class="col-9">
              <b>{{ application_details.phnumber }}</b>
            </div>
          </div>
          <div class="row">
            <div class="col-2">Realtion with</div>
            <div class="col-1">:</div>
            <div class="col-9">
              <b>{{ application_details.relation_with }}</b>
            </div>
          </div>
          <div class="row">
            <div class="col-2">{{ application_details.relation_with }} Name</div>
            <div class="col-1">:</div>
            <div class="col-9">
              <b>{{ application_details.relation_name }}</b>
            </div>
          </div>
          <div class="row">
            <div class="col-2">Gender</div>
            <div class="col-1">:</div>
            <div class="col-9">
              <b>{{ application_details.gender }}</b>
            </div>
          </div>
          <div class="row">
            <div class="col-2">Qualification</div>
            <div class="col-1">:</div>
            <div class="col-9">
              <b>{{ application_details.qualification }}</b>
            </div>
          </div>
          <div class="row">
            <div class="col-2">Emergency Phone number</div>
            <div class="col-1">:</div>
            <div class="col-9">
              <b>{{ application_details.emphnumber }}</b>
            </div>
          </div>
          <div class="row">
            <div class="col-2">Country</div>
            <div class="col-1">:</div>
            <div class="col-9">
              <b>{{ application_details.country }}</b>
            </div>
          </div>
          <div class="row">
            <div class="col-2">Blood Group</div>
            <div class="col-1">:</div>
            <div class="col-9">
              <b>{{ application_details.blood }}</b>
            </div>
          </div>
          <div class="row">
            <div class="col-2">Identifiction Mark 1</div>
            <div class="col-1">:</div>
            <div class="col-9">
              <b>{{ application_details.identificationmark1 }}</b>
            </div>
          </div>
          <div class="row">
            <div class="col-2">Identifiction Mark 2</div>
            <div class="col-1">:</div>
            <div class="col-9">
              <b>{{ application_details.identificationmark2 }}</b>
            </div>
          </div>
          <div class="row">
            <div class="col-2">Class of vehicle</div>
            <div class="col-1">:</div>
            <div class="col-9">
              <b>{{ application_details.classofvehicle }}</b>
            </div>
          </div>
          <br />
          <b>Permanent Address</b>
          <div class="row">
            <div class="col-3">House Name</div>
            <div class="col-1">:</div>
            <div class="col-8">
              <b>{{ application_details.prhousename }}</b>
            </div>
          </div>
          <div class="row">
            <div class="col-3">Location</div>
            <div class="col-1">:</div>
            <div class="col-8">
              <b>{{ application_details.prlocation }}</b>
            </div>
          </div>
          <div class="row">
            <div class="col-3">Street</div>
            <div class="col-1">:</div>
            <div class="col-8">
              <b>{{ application_details.prstreet }}</b>
            </div>
          </div>
          <div class="row">
            <div class="col-3">Taluk</div>
            <div class="col-1">:</div>
            <div class="col-8">
              <b>{{ application_details.prtaluk }}</b>
            </div>
          </div>
          <div class="row">
            <div class="col-3">Village</div>
            <div class="col-1">:</div>
            <div class="col-8">
              <b>{{ application_details.prvillage }}</b>
            </div>
          </div>
          <div class="row">
            <div class="col-3">Pincode</div>
            <div class="col-1">:</div>
            <div class="col-8">
              <b>{{ application_details.prpincode }}</b>
            </div>
          </div>
          <br />
          <b>Present Address</b>
          <div class="row">
            <div class="col-3">House Name</div>
            <div class="col-1">:</div>
            <div class="col-8">
              <b>{{ application_details.trhousename }}</b>
            </div>
          </div>
          <div class="row">
            <div class="col-3">Location</div>
            <div class="col-1">:</div>
            <div class="col-8">
              <b>{{ application_details.trlocation }}</b>
            </div>
          </div>
          <div class="row">
            <div class="col-3">Street</div>
            <div class="col-1">:</div>
            <div class="col-8">
              <b>{{ application_details.tstreet }}</b>
            </div>
          </div>
          <div class="row">
            <div class="col-3">Taluk</div>
            <div class="col-1">:</div>
            <div class="col-8">
              <b>{{ application_details.trtaluk }}</b>
            </div>
          </div>
          <div class="row">
            <div class="col-3">Village</div>
            <div class="col-1">:</div>
            <div class="col-8">
              <b>{{ application_details.trvillage }}</b>
            </div>
          </div>
          <div class="row">
            <div class="col-3">Pincode</div>
            <div class="col-1">:</div>
            <div class="col-8">
              <b>{{ application_details.trpincode }}</b>
            </div>
          </div>
          <br />
          <b>Documents uploaded</b>
          <div class="row">
            <div class="col-3">Identity Certificate</div>
            <div class="col-1">:</div>
            <div class="col-8">
              <span v-if="document_list.identitycertificate">
                <i
                  ><a
                    v-bind:href="
                      'http://localhost:8000' +
                      document_list.identitycertificate
                    "
                    target="__blank"
                    >click here</a
                  ></i
                >
              </span>
            </div>
          </div>
          <div class="row">
            <div class="col-3">Eye Certificate</div>
            <div class="col-1">:</div>
            <div class="col-8">
              <span v-if="document_list.eyecertificate">
                <i
                  ><a
                    v-bind:href="
                      'http://localhost:8000' + document_list.eyecertificate
                    "
                    target="__blank"
                    >click here</a
                  ></i
                >
              </span>
            </div>
          </div>
          <div class="row">
            <div class="col-3">Self Declaration Certificate</div>
            <div class="col-1">:</div>
            <div class="col-8">
              <span v-if="document_list.selfcertificate">
                <i
                  ><a
                    v-bind:href="
                      'http://localhost:8000' + document_list.selfcertificate
                    "
                    target="__blank"
                    >click here</a
                  ></i
                >
              </span>
            </div>
          </div>
          <br />
          <b>Other Documents</b><br>
          <span v-if="other_documents.length < 1"> No documents uploaded</span><br>
          <div
            class="row"
            v-for="document in other_documents"
            v-bind:key="document.id"
          >
            <div class="col-3">
              {{ document.document_name }}
            </div>
            <div class="col-1">:</div>
            <div class="col-8">
              <span v-if="document_list.medicalcertificate">
                <i
                  ><a
                    v-bind:href="'http://localhost:8000' + document.document"
                    target="__blank"
                    >click here</a
                  ></i
                >
              </span>
            </div>
          </div>
          <br />

          <form v-on:submit.prevent="StatusChangeRTO(application_details.id)" id="statusChange">
            <b>Update user Status</b><br>
                <i>**Only an RTO can update the below status of a User</i>
            <div style="margin-top: 2%">
                <div class="form-group">
                <b><label>Payment Status :</label>{{application_details.payment_status}}</b>
              </div>
              <div class="form-group">
                <label>Current User Status</label>{{application_details.user_status}}
                <select
                  v-model="application_details.user_status"
                  name="renewal_status"
                  class="form-control"
                  style="height:35px;"
                  required
                >
                <!-- Payment Completed, Waiting for approvall -->
                  <option value="Application Filled">Application Filled</option>
                  <option value="Documents Uploaded">Documents Uploaded</option>
                  <option value="Payment Completed, Waiting for approvall">
                    Payment Completed, Waiting for approvall
                  </option>
                  <option value="Approved">Approved</option>
                  <option value="Rejected">Rejected</option>
                  <option value="Resubmit">Resubmit</option>
                </select>
              </div>
              
              <div
                v-if="
                  application_details.user_status == 'Rejected' ||
                  application_details.user_status == 'Resubmit'
                "
                class="form-group"
              >
                <label
                  ><span style="color: red"
                    >Reason for rejecting the application*</span
                  ></label
                >
                <input v-model="application_details.reasonforrejecting" name="reasonforrejecting" type="text" class="form-control" required />
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
                <a href="/#/newapplicationlist">
                  <button type="button" class="btn btn-lg btn-primary">
                    Cancel
                  </button>
                </a>
              </div>
            </div>
          </form>
        </div>
      </div>
    </div>
  </div>
</template>
<script lang="ts" src="../ts/LicenceApplicationDetials.ts"></script>
<style scoped src="../css/UserList.css"></style>     
