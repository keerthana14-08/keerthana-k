# keerthana-k
JSON to POJO in JAVA 


package com.jsontopojo;
import java.util.ArrayList;
import java.util.HashMap;
import java.util.List;
import java.util.Map;
import com.fasterxml.jackson.annotation.JsonAnyGetter;
import com.fasterxml.jackson.annotation.JsonAnySetter;
import com.fasterxml.jackson.annotation.JsonIgnore;
import com.fasterxml.jackson.annotation.JsonInclude;
import com.fasterxml.jackson.annotation.JsonProperty;
import com.fasterxml.jackson.annotation.JsonPropertyOrder;
import org.apache.commons.lang.builder.EqualsBuilder;
import org.apache.commons.lang.builder.HashCodeBuilder;
import org.apache.commons.lang.builder.ToStringBuilder;

@JsonInclude(JsonInclude.Include.NON_NULL)
@JsonPropertyOrder({
    "about",
    "created",
    "id",
    "likes",
    "submitted"
})
public class Input {

    @JsonProperty("about")
    private String about;
    @JsonProperty("created")
    private String created;
    @JsonProperty("id")
    private Integer id;
    @JsonProperty("likes")
    private Integer likes;
    @JsonProperty("submitted")
    private List<Integer> submitted = new ArrayList<Integer>();
    @JsonIgnore
    private Map<String, Object> additionalProperties = new HashMap<String, Object>();

    @JsonProperty("about")
    public String getabout() {
        return about;
    }

    @JsonProperty("about")
    public void setName(String about) {
        this.about = about;
    }

    public Input withAbout(String about) {
        this.about = about;
        return this;
    }

    @JsonProperty("created")
    public String getCreated() {
        return created;
    }

    @JsonProperty("created")
    public void setCreated(String created) {
        this.created = created;
    }

    public Input withCreated(String created) {
        this.created = created;
        return this;
    }

    @JsonProperty("id")
    public Integer getId() {
        return id;
    }

    @JsonProperty("id")
    public void setId(Integer id) {
        this.id = id;
    }

    public Input withId(Integer id) {
        this.id = id;
        return this;
    }

    @JsonProperty("likes")
    public Integer getLikes() {
        return likes;
    }

    @JsonProperty("likes")
    public void setLikes(Integer likes) {
        this.likes = likes;
    }

    public Input withId(Integer likes) {
        this.likes =likes;
        return this;
    }

    @JsonProperty("submitted")
    public List<Integer> getsubmitted() {
        return submitted;
    }

    @JsonProperty("submitted")
    public void setSubmitted(List<Integer> submitted) {
        this.submitted = submitted;
    }

    public Input withSubmitted(List<Integer> submitted) {
        this.submitted = submitted;
        return this;
    }

    @Override
    public String toString() {
        return ToStringBuilder.reflectionToString(this);
    }

    @JsonAnyGetter
    public Map<String, Object> getAdditionalProperties() {
        return this.additionalProperties;
    }

    @JsonAnySetter
    public void setAdditionalProperty(String about, Object value) {
        this.additionalProperties.put(name, value);
    }

    public Input withAdditionalProperty(String about, Object value) {
        this.additionalProperties.put(name, value);
        return this;
    }

    @Override
    public int hashCode() {
        return new HashCodeBuilder().append(about).append(created).append(like).append(id).append(submitted).append(additionalProperties).toHashCode();
    }

    @Override
    public boolean equals(Object other) {
        if (other == this) {
            return true;
        }
        if ((other instanceof Input) == false) {
            return false;
        }
        Input rhs = ((Input) other);
        return new EqualsBuilder().append(about, rhs.about).append(created, rhs.created).append(like, rhs.like).append(id, rhs.id).append(submitted, rhs.submitted).append(additionalProperties, rhs.additionalProperties).isEquals();
    }

}
