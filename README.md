# MongoDbHandler
##### This file is a python logging Handler for MongoDb.
***    
## The correction is below
##### If 'msg' include letter ':',  occured error and didn't logging the error. This case will be logging levelname of 'critical'.
##### But If you don't want to be logging levename of 'critical', you can use following
          except InvalidDocument:
            err = sys.exc_info()[1]
            data['msg'] = str(err)
            data['levelname'] = 'critical'
            self.collection.insert_one(data)
