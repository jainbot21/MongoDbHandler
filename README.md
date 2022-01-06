# MongoDbHandler
##### This file is a python logging Handler for MongoDb.
***    
## The correction is below
##### If 'msg' include letter ':',  occured error and didn't logging the error. This case will be logging levelname of 'critical'.
##### If you don't want to be logging levename of 'critical', you can use following. But you won't be able to find the actual error content.
          '''python    
          except InvalidDocument:
                    data['msg'] = str(data['msg']).replace(':','')
                    self.collection.insert_one(data)
          '''
