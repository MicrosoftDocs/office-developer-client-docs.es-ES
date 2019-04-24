---
title: OpenStreamOnFileW
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- OpenStreamOnFileW
api_type:
- COM
ms.assetid: 263b9f24-eac8-4d34-8f66-dc87024b94b9
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 7e67d84320b57fe6e510b70a68088f289ef6030d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348870"
---
# <a name="openstreamonfilew"></a>OpenStreamOnFileW

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Asigna e inicializa un objeto OLE **IStream** para tener acceso al contenido de un archivo. Esta función toma cadenas uniCODE como argumentos, a diferencia de la versión ANSI de esta función [OpenStreamOnFile](openstreamonfile.md)y, por lo tanto, permite caracteres arbitrarios en el nombre de archivo que incluyan la ruta de acceso y la extensión de archivo.
  
|||
|:-----|:-----|
|ExPortado por:  <br/> |olmapi32. dll  <br/> |
|Implementado por:  <br/> |Outlook  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente y proveedores de servicios  <br/> |
   
```cpp
HRESULT STDMETHODCALLTYPE OpenStreamOnFileW(
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPFREEBUFFER lpFreeBuffer,
  ULONG ulFlags,
  LPWSTR lpszFileName,
  LPWSTR lpszPrefix,
  LPSTREAM FAR * lppStream
);
```

## <a name="parameters"></a>Parameters

 _lpAllocateBuffer_
  
> a Puntero a la función [MAPIAllocateBuffer](mapiallocatebuffer.md) , que se va a usar para asignar memoria. 
    
 _lpFreeBuffer_
  
> a Puntero a la función [MAPIFreeBuffer](mapifreebuffer.md) , que se usará para liberar memoria. 
    
 _ulFlags_
  
> a Máscara de la máscara utilizada para controlar la creación o la apertura del archivo al que se va a tener acceso a través del objeto OLE **IStream** . Se pueden establecer los siguientes indicadores: 
    
SOF_UNIQUEFILENAME
  
> Se debe crear un archivo temporal para el objeto **IStream** . Si se establece esta marca, también se deben establecer las marcas STGM_CREATE y STGM_READWRITE. 
    
STGM_CREATE
  
> El archivo se creará incluso si ya existe uno. Si no se establece el parámetro _lpszFileName_ , se deben establecer tanto este indicador como el STGM_DELETEONRELEASE. Si se establece STGM_CREATE, también se debe establecer la marca STGM_READWRITE. 
    
STGM_DELETEONRELEASE
  
> El archivo se eliminará cuando se libere el objeto **IStream** . Si no se establece el parámetro _lpszFileName_ , se deben establecer tanto este indicador como el STGM_CREATE. 
    
STGM_READ
  
> El archivo se va a crear o abrir con acceso de solo lectura.
    
STGM_READWRITE
  
> El archivo se va a crear o abrir con permiso de lectura y escritura. Si no se establece esta marca, no se debe establecer tampoco la marca STGM_CREATE.
    
 _lpszFileName_
  
> a El nombre de archivo, incluida la ruta de acceso y la extensión, del archivo denominado Unicode para el que **OpenStreamOnFileW** inicializa el objeto **IStream** . Si se establece la marca SOF_UNIQUEFILENAME, _lpszFileName_ contiene la ruta de acceso al directorio en el que se va a crear un archivo temporal. Si _lpszFileName_ es null, **OpenStreamOnFileW** obtiene una ruta de acceso adecuada del sistema y se deben establecer los dos marcadores STGM_CREATE y STGM_DELETEONRELEASE. 
    
 _lpszPrefix_
  
> a Prefijo del nombre de archivo Unicode en el que **OpenStreamOnFileW** inicializa el objeto **IStream** . Si se establece, el prefijo no debe contener más de tres caracteres. Si _lpszPrefix_ es null, se usa un prefijo de "Sof". 
    
 _lppStream_
  
> contempla Puntero a un puntero a un objeto que expone la interfaz **IStream** . 
    
## <a name="return-value"></a>Valor devuelto

S_OK
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
MAPI_E_NO_ACCESS
  
> No se pudo tener acceso al archivo debido a que los permisos de usuario son insuficientes o a que no se pueden modificar los archivos de solo lectura.
    
MAPI_E_NOT_FOUND
  
> El archivo designado no existe.
    
## <a name="remarks"></a>Comentarios

La función **OpenStreamOnFileW** tiene dos usos importantes además de controlar un archivo con un nombre Unicode, que se distingue por el valor de la marca SOF_UNIQUEFILENAME. Si no se establece esta marca, **OpenStreamOnFileW** abre un objeto **IStream** en un archivo existente, por ejemplo, para copiar su contenido en la propiedad **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) de un dato adjunto mediante el ** Método IStream:: CopyTo** . En este caso, el parámetro _lpszFileName_ especifica la ruta de acceso y el nombre del archivo. 
  
Cuando se establece SOF_UNIQUEFILENAME, **OpenStreamOnFileW** crea un archivo temporal para contener los datos de un objeto **IStream** . Para este uso, el parámetro _lpszFileName_ puede designar opcionalmente la ruta de acceso al directorio en el que se va a crear el archivo, y el parámetro _lpszPrefix_ puede especificar opcionalmente un prefijo para el nombre de archivo. 
  
Cuando finaliza la aplicación cliente o el proveedor de servicios que realiza la llamada con el objeto **IStream** , debe liberarla llamando al método OLE **IStream:: Release** . 
  
MAPI usa las funciones a las que apunta _lpAllocateBuffer_ y _lpFreeBuffer_ para la mayor parte de la asignación y desasignación de memoria, en particular para asignar memoria para que la usen las aplicaciones cliente al llamar a interfaces de objeto como [IMAPIProp:: GetProps](imapiprop-getprops.md) y [IMAPITable:: QueryRows](imapitable-queryrows.md). 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

La marca SOF_UNIQUEFILENAME se usa para crear un archivo temporal con un nombre único para el sistema de mensajería. Si se establece esta marca, el parámetro _lpszFileName_ especifica la ruta de acceso del archivo temporal y el parámetro _lpszPrefix_ contiene los caracteres de prefijo del nombre de archivo. El nombre de archivo <prefix>construido es HHHH TMP, donde HHHH es un número hexadecimal. Si _lpszFileName_ es null, el archivo se creará en el directorio de archivos temporales que devuelve la función de Windows **GetTempPath**, o el directorio actual, si no se ha designado ningún directorio de archivos temporales.
  
Si no se establece la marca SOF_UNIQUEFILENAME, se omite _lpszPrefix_ y _lpszFileName_ debe contener la ruta de acceso completa y el nombre de archivo del archivo que se va a abrir o crear. El archivo se abrirá o se creará en función de los demás indicadores establecidos en _ulFlags_.
  
## <a name="see-also"></a>Vea también



[OpenStreamOnFile](openstreamonfile.md)

