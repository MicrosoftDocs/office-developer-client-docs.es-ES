---
title: OpenStreamOnFile
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.OpenStreamOnFile
api_type:
- COM
ms.assetid: 01fa459f-597d-4b16-b340-a79fb270cd71
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: b05f5b30eceb7df1bed76c64f4bdda87ede0e463
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439096"
---
# <a name="openstreamonfile"></a>OpenStreamOnFile

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Asigna e inicializa un objeto OLE **IStream** para tener acceso al contenido de un archivo. Esta función toma una cadena ANSI como nombre de archivo, incluida la ruta de acceso y la extensión de archivo; por lo tanto, se recomienda el uso de la versión Unicode de esta función, [OpenStreamOnFileW.](openstreamonfilew.md)
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente y proveedores de servicios  <br/> |
   
```cpp
HRESULT STDMETHODCALLTYPE OpenStreamOnFile(
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPFREEBUFFER lpFreeBuffer,
  ULONG ulFlags,
  LPSTR lpszFileName,
  LPSTR lpszPrefix,
  LPSTREAM FAR * lppStream
);
```

## <a name="parameters"></a>Parámetros

 _lpAllocateBuffer_
  
> [entrada] Puntero a la [función MAPIAllocateBuffer,](mapiallocatebuffer.md) que se usará para asignar memoria. 
    
 _lpFreeBuffer_
  
> [entrada] Puntero a la [función MAPIFreeBuffer,](mapifreebuffer.md) que se usará para liberar memoria. 
    
 _ulFlags_
  
> [entrada] Máscara de bits de marcas usadas para controlar la creación o apertura del archivo al que se debe tener acceso a través del objeto **OLE IStream** . Se pueden establecer las siguientes marcas: 
    
SOF_UNIQUEFILENAME 
  
> Se creará un archivo temporal para el **objeto IStream.** Si se establece esta marca, también STGM_CREATE y STGM_READWRITE marca. 
    
STGM_CREATE 
  
> El archivo se creará incluso si ya existe uno. Si no se establece el parámetro  _lpszFileName,_ se deben establecer tanto esta marca STGM_DELETEONRELEASE como el parámetro. Si STGM_CREATE se establece, también STGM_READWRITE debe establecerse la marca de STGM_READWRITE. 
    
STGM_DELETEONRELEASE 
  
> El archivo se eliminará cuando se libera el objeto **IStream.** Si no se establece el parámetro  _lpszFileName,_ se deben establecer tanto esta marca STGM_CREATE como el parámetro. 
    
STGM_READ 
  
> El archivo se va a crear o abrir con acceso de solo lectura. 
    
STGM_READWRITE 
  
> El archivo se va a crear o abrir con permiso de lectura y escritura. Si no se establece esta marca, la STGM_CREATE no debe establecerse. 
    
 _lpszFileName_
  
> [entrada] Nombre de archivo, incluida la ruta de acceso y la extensión, del archivo para el que **OpenStreamOnFile** inicializa el **objeto IStream.** Si se SOF_UNIQUEFILENAME marca,  _lpszFileName_ contiene la ruta de acceso al directorio en el que se va a crear un archivo temporal. Si  _lpszFileName_ es NULL, **OpenStreamOnFile** obtiene una ruta de acceso adecuada del sistema y se deben establecer las marcas STGM_CREATE y STGM_DELETEONRELEASE. 
    
 _lpszPrefix_
  
> [entrada] Prefijo del nombre de archivo en el que **OpenStreamOnFile** inicializa el **objeto IStream.** Si se establece, el prefijo no debe contener más de tres caracteres. Si  _lpszPrefix_ es NULL, se usa un prefijo de "SOF". 
    
 _lppStream_
  
> [salida] Puntero a un puntero a un objeto que expone la **interfaz IStream.** 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores. 
    
MAPI_E_NO_ACCESS 
  
> No se pudo tener acceso al archivo debido a que los permisos de usuario no son suficientes o porque no se pueden modificar los archivos de solo lectura. 
    
MAPI_E_NOT_FOUND 
  
> El archivo designado no existe.
    
## <a name="remarks"></a>Comentarios

La **función OpenStreamOnFile** tiene dos usos importantes, que se distinguen por la configuración de SOF_UNIQUEFILENAME marca. Cuando no se establece esta marca, **OpenStreamOnFile** abre un objeto **IStream** en un archivo existente, por ejemplo, para copiar su contenido en la propiedad **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) de un archivo adjunto mediante el método **IStream::CopyTo.** En este caso,  _el parámetro lpszFileName_ especifica la ruta de acceso y el nombre de archivo del archivo. 
  
Cuando SOF_UNIQUEFILENAME se establece, **OpenStreamOnFile** crea un archivo temporal para contener los datos de un **objeto IStream.** Para este uso, el parámetro  _lpszFileName_ puede designar opcionalmente la ruta de acceso al directorio donde se va a crear el archivo y el parámetro  _lpszPrefix_ puede especificar opcionalmente un prefijo para el nombre de archivo. 
  
Cuando la aplicación cliente de llamada o el proveedor de servicios termine con el objeto **IStream,** debe liberarlo llamando al método OLE **IStream::Release.** 
  
MAPI usa las funciones a las que  _apuntan lpAllocateBuffer_ y  _lpFreeBuffer_ para la mayor parte de la asignación y desasignación de memoria, en particular para asignar memoria para que la usen las aplicaciones cliente al llamar a interfaces de objetos como [IMAPIProp::GetProps](imapiprop-getprops.md) e [IMAPITable::QueryRows](imapitable-queryrows.md). 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

La SOF_UNIQUEFILENAME se usa para crear un archivo temporal con un nombre único para el sistema de mensajería. Si se establece esta marca, el parámetro  _lpszFileName_ especifica la ruta de acceso para el archivo temporal y el parámetro  _lpszPrefix_ contiene los caracteres de prefijo del nombre de archivo. El nombre de archivo construido es <prefix> HHHH. TMP, donde HHHH es un número hexadecimal. Si  _lpszFileName_ es NULL, el archivo se creará en el directorio de archivos temporales que se devuelve de la función de Windows **GetTempPath** o en el directorio actual si no se ha designado ningún directorio de archivos temporales. 
  
Si no se SOF_UNIQUEFILENAME marca, se omite  _lpszPrefix_ y  _lpszFileName_ debe contener la ruta de acceso completa y el nombre de archivo del archivo que se va a abrir o crear. El archivo se abrirá o creará en función de las demás marcas establecidas en  _ulFlags_. 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|File.cpp  <br/> |WriteAttachStreamToFile  <br/> |MFCMAPI usa el **método OpenStreamOnFile** para abrir una secuencia en un archivo para que se puedan escribir datos adjuntos en él.  <br/> |
   
## <a name="see-also"></a>Consulte también



[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

