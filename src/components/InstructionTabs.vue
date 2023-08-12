<template>
  <div class="tabs is-small">
    <ul>
      <li :class="{ 'is-active': state.activeTab === 'gmail' }">
        <a @click="state.activeTab = 'gmail'">Gmail (Web)</a>
      </li>
      <li :class="{ 'is-active': state.activeTab === 'applemail' }">
        <a @click="state.activeTab = 'applemail'">Apple Mail (Desktop)</a>
      </li>
      <!-- <li :class="{ 'is-active': state.activeTab === 'outlook' }">
        <a @click="state.activeTab = 'outlook'">Outlook.com (Web)</a>
      </li> -->
      <li :class="{ 'is-active': state.activeTab === 'outlookdesktop' }">
        <a @click="state.activeTab = 'outlookdesktop'">Outlook (Desktop)</a>
      </li>
    </ul>
  </div>
  <div class="tab-content">
    <div
      :class="{ 'is-active': state.activeTab === 'gmail', 'tab-inner': true }"
    >
      <div class="content">
        <ol class="steps">
          <li>
            Once logged into your Gmail account, click the settings cog icon <svg width="15" height="15" viewBox="0 0 15 15" fill="none" xmlns="http://www.w3.org/2000/svg"><path d="M7.07095 0.650238C6.67391 0.650238 6.32977 0.925096 6.24198 1.31231L6.0039 2.36247C5.6249 2.47269 5.26335 2.62363 4.92436 2.81013L4.01335 2.23585C3.67748 2.02413 3.23978 2.07312 2.95903 2.35386L2.35294 2.95996C2.0722 3.2407 2.0232 3.6784 2.23493 4.01427L2.80942 4.92561C2.62307 5.2645 2.47227 5.62594 2.36216 6.00481L1.31209 6.24287C0.924883 6.33065 0.650024 6.6748 0.650024 7.07183V7.92897C0.650024 8.32601 0.924883 8.67015 1.31209 8.75794L2.36228 8.99603C2.47246 9.375 2.62335 9.73652 2.80979 10.0755L2.2354 10.9867C2.02367 11.3225 2.07267 11.7602 2.35341 12.041L2.95951 12.6471C3.24025 12.9278 3.67795 12.9768 4.01382 12.7651L4.92506 12.1907C5.26384 12.377 5.62516 12.5278 6.0039 12.6379L6.24198 13.6881C6.32977 14.0753 6.67391 14.3502 7.07095 14.3502H7.92809C8.32512 14.3502 8.66927 14.0753 8.75705 13.6881L8.99505 12.6383C9.37411 12.5282 9.73573 12.3773 10.0748 12.1909L10.986 12.7653C11.3218 12.977 11.7595 12.928 12.0403 12.6473L12.6464 12.0412C12.9271 11.7604 12.9761 11.3227 12.7644 10.9869L12.1902 10.076C12.3768 9.73688 12.5278 9.37515 12.638 8.99596L13.6879 8.75794C14.0751 8.67015 14.35 8.32601 14.35 7.92897V7.07183C14.35 6.6748 14.0751 6.33065 13.6879 6.24287L12.6381 6.00488C12.528 5.62578 12.3771 5.26414 12.1906 4.92507L12.7648 4.01407C12.9766 3.6782 12.9276 3.2405 12.6468 2.95975L12.0407 2.35366C11.76 2.07292 11.3223 2.02392 10.9864 2.23565L10.0755 2.80989C9.73622 2.62328 9.37437 2.47229 8.99505 2.36209L8.75705 1.31231C8.66927 0.925096 8.32512 0.650238 7.92809 0.650238H7.07095ZM4.92053 3.81251C5.44724 3.44339 6.05665 3.18424 6.71543 3.06839L7.07095 1.50024H7.92809L8.28355 3.06816C8.94267 3.18387 9.5524 3.44302 10.0794 3.81224L11.4397 2.9547L12.0458 3.56079L11.1882 4.92117C11.5573 5.44798 11.8164 6.0575 11.9321 6.71638L13.5 7.07183V7.92897L11.932 8.28444C11.8162 8.94342 11.557 9.55301 11.1878 10.0798L12.0453 11.4402L11.4392 12.0462L10.0787 11.1886C9.55192 11.5576 8.94241 11.8166 8.28355 11.9323L7.92809 13.5002H7.07095L6.71543 11.932C6.0569 11.8162 5.44772 11.5572 4.92116 11.1883L3.56055 12.046L2.95445 11.4399L3.81213 10.0794C3.4431 9.55266 3.18403 8.94326 3.06825 8.2845L1.50002 7.92897V7.07183L3.06818 6.71632C3.18388 6.05765 3.44283 5.44833 3.81171 4.92165L2.95398 3.561L3.56008 2.95491L4.92053 3.81251ZM9.02496 7.50008C9.02496 8.34226 8.34223 9.02499 7.50005 9.02499C6.65786 9.02499 5.97513 8.34226 5.97513 7.50008C5.97513 6.65789 6.65786 5.97516 7.50005 5.97516C8.34223 5.97516 9.02496 6.65789 9.02496 7.50008ZM9.92496 7.50008C9.92496 8.83932 8.83929 9.92499 7.50005 9.92499C6.1608 9.92499 5.07513 8.83932 5.07513 7.50008C5.07513 6.16084 6.1608 5.07516 7.50005 5.07516C8.83929 5.07516 9.92496 6.16084 9.92496 7.50008Z" fill="currentColor" fill-rule="evenodd" clip-rule="evenodd"></path></svg> in the
            top right corner.
          </li>
          <li>Select the <span class="has-text-weight-medium">See all settings</span> button.</li>
          <li>Scroll down to the <span class="has-text-weight-medium">Signature</span> section and click <span class="has-text-weight-medium">"Create new"</span>.</li>
          <li>
            Enter your new signature name into the popup and click <span class="has-text-weight-medium">"Create"</span>.
          </li>
          <li>Copy and paste your signature into the signature text box.</li>
          <li>
            <p>
              Choose your new signature in the <span class="has-text-weight-medium">"For New Emails Use"</span> dropdown.
            </p>
          </li>
          <li>
            Ensure you scroll the bottom of the page and click <span class="has-text-weight-medium">Save Changes</span>.
          </li>
        </ol>
        <p>
          <span class="tag is-info is-light is-rounded">Note</span> If you are using Google Chrome, there can be a bug with where pasting the signature in causes your signature's links to appear <span class="is-underlined">underlined</span>. If it bothers you, you can switch to a browser such as Firefox to resolve the issue, then go back to Chrome once you have saved it.
        </p>
      </div>
    </div>
    <!-- <div
      :class="{ 'is-active': state.activeTab === 'outlook', 'tab-inner': true }"
    >
      <div class="content">
        <ol class="steps">
          <li>
            Once logged into your Outlook.com account, click the <span class="has-text-weight-medium">Settings</span> Cog in
            the top right corner.
          </li>
          <li>
            With the sidebar settings menu open click <span class="has-text-weight-medium">View All Outlook Settings</span>
            in the bottom right corner.
          </li>
          <li>
            Select the <span class="has-text-weight-medium">Mail</span> tab and then <span class="has-text-weight-medium">Signatures</span> tab in the settings
            modal.
          </li>
          <li>
            Copy and paste your new email signature into the signature editor.
            <p>
              Please ensure that the <span class="has-text-weight-medium">"Compose messages in HTML format"</span> setting
              is correct and that you have checked the appropriate checkboxes
              around automatically using this signature.
            </p>
          </li>
          <li>Click <span class="has-text-weight-medium">Save</span> and exit the settings modal.</li>
        </ol>
      </div>
    </div> -->
    <div
      :class="{
        'is-active': state.activeTab === 'outlookdesktop',
        'tab-inner': true,
      }"
    >
      <div class="content">
        <div class="notification is-warning is-light">
          <strong>Note:</strong>
          Outlook infamously uses the Microsoft Word rendering engine for email
          which will cause differences to your signature preview. For many of
          your recipients, links will appear with a blue underline, spacing and
          font sizing will appear differently and images may not display at all.
          <br />
          If you care about your email signature being "pixel perfect" then you
          should use an email client that uses a HTML rendering engine, like
          Gmail.com.
        </div>
        <ol class="steps">
          <li>
            With Outlook open, click the <span class="has-text-weight-medium">New Email</span> button to bring up the email
            composer.
          </li>
          <li>
            Click <span class="has-text-weight-medium">Signature</span> in the message toolbar and then the <span class="has-text-weight-medium">Signatures</span>
            option to open the Signature Settings modal.
          </li>
          <li>
            Select the existing signature you'd like to edit or click <span class="has-text-weight-medium">New</span> to
            create one.
          </li>
          <li>Copy and paste your signature into the signature editor.</li>
          <li>Click <span class="has-text-weight-medium">OK</span> to exit the Signature Settings modal.</li>
          <li>
            <p>
              Now under the Signature option in the message toolbar you should
              see your signature. From this dropdown click your signature to
              insert it into the email body.
            </p>
          </li>
        </ol>
        <p>
          <span class="tag is-info is-light is-rounded">Still not working properly?</span> Try pasting the signature into a Word document and then copying it from there.
        </p>
      </div>
    </div>
    <div
      :class="{
        'is-active': state.activeTab === 'applemail',
        'tab-inner': true,
      }"
    >
      <div class="content">
        <ol class="steps">
          <li>
            With the Mail application open, click <span class="has-text-weight-medium">Mail</span> and then <span class="has-text-weight-medium">Preferences</span> in
            the top left corner of your screen.
          </li>
          <li>From the preferences pop-up, click the <span class="has-text-weight-medium">Signatures</span> tab.</li>
          <li>Click the <span class="has-text-weight-medium">+</span> button at the bottom of the middle column.</li>
          <li>
            Copy and paste your new email signature into the right-hand column
            and close the pop-up window to save.
            <p>
              In this preview the images will appear blank. Don't worry – once
              you actaully go to compose an email the images will appear.
            </p>
            <p>
              <span class="tag is-warning is-light is-rounded">Important</span> Ensure that <span class="has-text-weight-medium">"Always
              match my default message font"</span> is unchecked, otherwise your
              signature will appear in plain text.
            </p>
            <p>
              <span class="tag is-warning is-light is-rounded">Important</span> Still seeing a plain
              text version? Try toggling the <span class="has-text-weight-medium">"Place signature above quoted text"</span>
              checkbox and pasting in your signature again.
            </p>
          </li>
          <li>
            Select your new signature in the <span class="has-text-weight-medium">"Choose Signature"</span> field near the
            bottom of the pop-up.
          </li>
          <li>
            <p>
              <span class="tag is-warning is-light is-rounded">Important</span> Images not appearing
              when you compose an email? Go to your <span class="has-text-weight-medium">Privacy settings</span> and ensure
              that
              <span class="has-text-weight-medium">Block All Remote Content</span> is
              unchecked.
            </p>
          </li>
        </ol>
      </div>
    </div>
  </div>
</template>

<script setup>
import { reactive } from "vue";
const state = reactive({
  activeTab: "gmail",
});
</script>

<style scoped>
.tab-inner {
  display: none;
}

.tab-inner.is-active {
  display: block;
}
</style>
