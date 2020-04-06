# git-training

def snappy_compress(path):
    path_to_store = path+'.snappy'
    with open(path,'rb') as in_file:
        with open(path_to_store, 'wb') as out_file:
            snappy.stream_compress(in_file,out_file)
            out_file.close()
            in_file.close()
    return path_to_store

snappy_compress(r'C:\Users\show2\Downloads\input.csv')


def snappy_decompress(path):
    path_to_store = path+'.desnappy'
    with open(path,'rb') as in_file:
        with open(path_to_store, 'wb') as out_file:
            snappy.stream_decompress(in_file,out_file)
            out_file.close()
            in_file.close()
    return path_to_store
snappy_decompress(r'C:\Users\show2\Downloads\input.csv.snappy')
