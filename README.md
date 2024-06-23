# Speech Emotion Recognition (SER) for Enhanced Public Safety

## Project Overview

This project aims to develop a robust Speech Emotion Recognition (SER) model capable of detecting various emotions in a person's voice, particularly focusing on security applications. By analyzing vocal patterns, the model can identify stressful situations, such as fear or stress, suggesting potential danger and the need for immediate assistance. Additionally, this project includes a geospatial analysis of detected emotions to create hotspot maps, providing valuable insights for security management, urban planning, and public safety enhancement.

## Significance of the Problem

The application of SER in public security offers several significant benefits:

- **Early Threat Detection**: Identifies potential threats through early detection of distress or unusual behaviors in speech.
- **Non-Intrusive Monitoring**: Provides a privacy-conscious alternative to traditional invasive surveillance methods.
- **Contextual Awareness**: Enhances security systems by understanding the emotional context of conversations.
- **Crowd Surveillance**: Offers insights into the overall mood in crowded areas, aiding in managing large gatherings.
- **Automated Alerts**: Enables automated alerts for timely responses to potential threats.
- **Smart City Applications**: Integrates with other technologies to create safer urban environments.
- **Preventing Criminal Activities**: Helps in preventing criminal activities by detecting stress, fear, or aggression in speech.
- **Public Safety and Well-Being**: Contributes to public safety and well-being through efficient, privacy-respecting security measures.

## Datasets Used

1. **RAVDESS**: Contains speech in various emotional tones.
2. **TESS**: Toronto Emotional Speech Set for evaluating emotion recognition.
3. **CREMA**: Features diverse speakers and emotional tones.
4. **SAVEE**: Surrey Audio-Visual Expressed Emotion, focusing on British English speech.

## Data Preprocessing

- **Standardization**: Emotions were mapped to standardized labels for consistency across datasets.
- **Concatenation**: Datasets were combined to form a comprehensive dataframe with a total of 12,162 entries.

## Data Augmentation

Techniques used to increase the size and variability of the dataset included:

- Noise Addition
- Stretching
- Shifting
- Pitch Change

After augmentation, the total dataset size increased to 48,648 entries.

## Feature Extraction

Key features extracted using the `librosa` library included:

- Zero-Crossing Rate
- Chroma STFT
- MFCC (Mel-Frequency Cepstral Coefficients)
- RMS (Root Mean Square)
- Mel Spectrogram

These features formed a comprehensive feature matrix for each audio file.

## Model Training

Three models were trained on the extracted features:

### Convolutional Neural Network (CNN)

- **Training Time**: 252.95 seconds
- **Test Accuracy**: 60.49%
- **Performance**: Strong in recognizing 'angry' and 'surprise' emotions.

### Recurrent Neural Network (RNN)

- **Training Time**: 273.77 seconds
- **Test Accuracy**: 28.72%
- **Performance**: Low accuracy, struggled with recognizing emotions.

### Long Short-Term Memory (LSTM)

- **Training Time**: 1948.70 seconds
- **Test Accuracy**: 67.13%
- **Performance**: Best overall performance, high precision and recall for 'angry', 'calm', 'surprise', and 'fear' emotions.

## Model Comparison

- **LSTM**: Highest accuracy, best at capturing temporal dependencies in speech data.
- **CNN**: Moderate performance, faster training time.
- **RNN**: Least effective, struggled with complexity.

## Geographical Visualization of Fear Emotion Hotspots

Using Folium, a Python library for mapping data, the geographical visualization of fear emotion hotspots was created, revealing clusters indicating hotspots where fear emotion was more frequently expressed.

## Conclusion

The LSTM model demonstrated the best performance in recognizing emotions from speech, followed by the CNN model. Data augmentation and feature extraction significantly enhanced model performance. The geographical visualization provided insights into the distribution of fear emotions, helping identify patterns and clusters of emotional responses.

## Future Work

- **Human-Computer Interaction (HCI) Research**: Investigate user experience and refine HCI elements.
- **Long-Term Impact Assessment**: Evaluate the enduring impact of SER implementation on road security.
- **Privacy-Preserving Techniques**: Explore methods like federated learning to address privacy concerns.
- **Public Awareness Initiatives**: Educate the public about the benefits and limitations of SER.
- **International Collaboration**: Exchange insights with global research institutions.
- **Policy Advocacy**: Contribute to the formulation of ethical guidelines for SER usage.
- **Robustness Testing**: Test the SER system's resilience across diverse conditions.
- **Integration with Smart City Initiatives**: Explore opportunities for broader integration in urban development.

## Visualizations

### Waveplot, Spectrum, and Mel-spectrogram

- Angry Emotion
- Disgust Emotion
- Fear Emotion
- Happy Emotion
- Neutral Emotion
- Sad Emotion
- Surprise Emotion

### Additional Plots

- Zero-Crossing Rate (ZCR) vs. Time
- Time vs. Pitch Class (Chroma-stft)
- Time vs. MFCC (MFCCs)

## Contact

For more information or to contribute to this project, please contact:

- **GitHub**: [HimanshiBaliyan](https://HimanshiBaliyan)

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.
