# CMSC320 Final Tutorial --- By: Isabella Battish, Janet Choi, and Sarah Hwang

      },
      "execution_count": null,
      "outputs": []
    },
    {
      "cell_type": "code",
      "source": [
        "sns.lineplot(x='YEAR', y='month_moisture', hue= 'State',\n",
        "             data=df)"
      ],
      "metadata": {
        "id": "l86Lmy5qliiX"
      },
      "execution_count": null,
      "outputs": []
    },
    {
      "cell_type": "markdown",
      "source": [
        "The next thing we want to see is if there is a relationship between the amount of monthly moisture and the source of a municipalities drinking water. Maybe if a place is dry they'll be more likely to use ground water or purchased water?"
      ],
      "metadata": {
        "id": "nY5IEo5IntxX"
      }
    },
    {
      "cell_type": "code",
      "source": [
        "sns.violinplot(x='PRIMARY_SOURCE_CODE', y='month_moisture',\n",
        "             data=df)"
      ],
      "metadata": {
        "id": "aEZ8PGd1ns4F"
      },
      "execution_count": null,
      "outputs": []
    },
    {
      "cell_type": "markdown",
      "source": [
        "Interesting, again we don't see tons of variance. The only point of interest is that areas that have purchased groundwater are more likely to have a higher moisture.\n",
        "\n",
        "The last thing we'll look at is, if the 2012 drought influenced how much money municipalities spent on water. To do this, we'll look at the cost of water utilities before 2012, and during 2012."
      ],
      "metadata": {
        "id": "nGzLBBfzqVNK"
      }
    },
    {
      "cell_type": "code",
      "source": [
        "df_pre2012= df.loc[df['YEAR'] <= 2012]\n",
        "\n",
        "sns.lineplot(x= \"YEAR\", y= \"Water_Util_Total_Exp\", data= df_pre2012)"
      ],
      "metadata": {
        "id": "sfF7XYEBXxxh"
      },
      "execution_count": null,
      "outputs": []
    },
    {
      "cell_type": "markdown",
      "source": [
        "So hear we noticed that the amount spent on water utilities by municipalities does increase from 1997 to 2007 but plateaus from 2007 to 2012. This doesn't support our suspicion that the 2012 drough would cause municipalities to spend more on water."
      ],
      "metadata": {
        "id": "Y_YDJneQXX69"
      }
    }
  ]
}
