https://labs.cognitiveclass.ai/tools/jupyterlab/


pastaPlaceRating =[
            {'Category':'Fast Food Restaurant', 'rating':5},
            {'Category':'Thai Restaurant', 'rating':4.5},
            {'Category':'Mexican Restaurant', 'rating':3},
            {'Category':'Asian Restaurant', 'rating':2.5},
            {'Category':"Italian Restaurant", 'rating':2}
         ] 

pastaPlaceRatingDf = pd.DataFrame(restaurantCategories)
pastaPlaceRatingDf.insert(1, "rating", 1.0)
pastaPlaceRatingDf.rename(columns={0:"category"}, inplace=True)


# pastaPlaceRatingDf[pastaPlaceRatingDf["category"].isin(["Thai Restaurant"])]["rating"]=2.0
pastaPlaceRatingDf.loc([pastaPlaceRatingDf["category"].isin(["Thai Restaurant"])]["rating"]=2.0

# [rating for rating in pastaPlaceRating if rating in pastaPlaceRating["category"]]
# [pastaPlaceRatingDf[pastaPlaceRatingDf["category"] == rating]["rating"]=2.0 for rating in pastaPlaceRating]