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
ms.openlocfilehash: 9f37e57f997ead58b1ef0e9a27ccbdb0a810be06
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571958"
---
# <a name="openstreamonfile"></a>OpenStreamOnFile

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Asigna e inicializa un objeto **IStream** OLE para tener acceso al contenido de un archivo. Esta función toma una cadena ANSI como el nombre de archivo, incluida la ruta de acceso y la extensión de archivo, por lo tanto, uso de la versión de Unicode de esta función, [OpenStreamOnFileW](openstreamonfilew.md), se recomienda.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Las aplicaciones cliente y los proveedores de servicios  <br/> |
   
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
  
> [entrada] Puntero a la función [MAPIAllocateBuffer](mapiallocatebuffer.md) , que se usará para asignar memoria. 
    
 _lpFreeBuffer_
  
> [entrada] Puntero a la función [MAPIFreeBuffer](mapifreebuffer.md) , que se usará para liberar memoria. 
    
 _ulFlags_
  
> [entrada] Máscara de bits de indicadores que se utilizan para controlar la creación o apertura del archivo para tener acceso a través del objeto **IStream** OLE. Se pueden establecer los siguientes indicadores: 
    
SOF_UNIQUEFILENAME 
  
> Es un archivo temporal que se creará para el objeto **IStream** . Si se establece este marcador, también se deben establecer los indicadores STGM_CREATE y STGM_READWRITE. 
    
STGM_CREATE 
  
> Es el archivo que se creará, incluso si ya existe una. Si no se establece el parámetro _lpszFileName_ , se deben establecer este indicador y el STGM_DELETEONRELEASE. Si se establece STGM_CREATE, también se debe establecer la marca STGM_READWRITE. 
    
STGM_DELETEONRELEASE 
  
> Es el archivo que se eliminará cuando se libera el objeto **IStream** . Si no se establece el parámetro _lpszFileName_ , se deben establecer este indicador y el STGM_CREATE. 
    
STGM_READ 
  
> El archivo es que se creen o se abrió con acceso de solo lectura. 
    
STGM_READWRITE 
  
> Es el archivo que se creó o se abran con permiso de lectura y escritura. Si no se establece este indicador, el indicador STGM_CREATE no debe establecerse cualquiera. 
    
 _lpszFileName_
  
> [entrada] El nombre de archivo, incluida la ruta de acceso y la extensión del archivo para el que **OpenStreamOnFile** inicializa el objeto **IStream** . Si se establece la marca SOF_UNIQUEFILENAME, _lpszFileName_ contiene la ruta de acceso al directorio en el que se va a crear un archivo temporal. Si _lpszFileName_ es NULL, **OpenStreamOnFile** Obtiene una ruta de acceso apropiado desde el sistema y se deben establecer el STGM_CREATE y la STGM_DELETEONRELEASE marcas. 
    
 _lpszPrefix_
  
> [entrada] El prefijo del nombre de archivo en el que **OpenStreamOnFile** inicializa el objeto **IStream** . Si se establece, el prefijo debe contener no más de tres caracteres. Si _lpszPrefix_ es NULL, se utiliza un prefijo de "SOF". 
    
 _lppStream_
  
> [out] Puntero a un puntero a un objeto que expone la interfaz **IStream** . 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores. 
    
MAPI_E_NO_ACCESS 
  
> No se pudo tener acceso el archivo debido a los permisos de usuario suficientes o debido a que no se pueden modificar los archivos de sólo lectura. 
    
MAPI_E_NOT_FOUND 
  
> No existe el archivo designado.
    
## <a name="remarks"></a>Comentarios

La función **OpenStreamOnFile** tiene dos usos importantes, diferenciados por la configuración de la marca SOF_UNIQUEFILENAME. Cuando no se establece este marcador, **OpenStreamOnFile** se abre un objeto **IStream** en un archivo existente, por ejemplo, para copiar su contenido en la propiedad **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) de los datos adjuntos con el **IStream :: CopyTo** (método). En este caso, el parámetro _lpszFileName_ especifica la ruta de acceso y el nombre del archivo. 
  
Cuando se establece SOF_UNIQUEFILENAME, **OpenStreamOnFile** crea un archivo temporal para contener datos para un objeto **IStream** . Para este uso, el parámetro _lpszFileName_ , opcionalmente, puede designar la ruta de acceso al directorio donde es el archivo que se creará y el parámetro _lpszPrefix_ , opcionalmente, puede especificar un prefijo para el nombre de archivo. 
  
Cuando finalice la aplicación cliente que llama o el proveedor de servicios con el objeto **IStream** , que debe liberar llamando al método OLE **IStream:: Release** . 
  
MAPI utiliza las funciones que señala _lpAllocateBuffer_ y _lpFreeBuffer_ para la mayoría de asignación de memoria y cancelación de asignación, en particular para asignar la memoria para su uso por las aplicaciones cliente al llamar a las interfaces de objeto como [IMAPIProp:: GetProps](imapiprop-getprops.md) e [IMAPITable:: QueryRows](imapitable-queryrows.md). 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

El indicador SOF_UNIQUEFILENAME se utiliza para crear un archivo temporal con un nombre único para el sistema de mensajería. Si se establece este indicador, el _lpszFileName_ parámetro especifica la ruta de acceso para el archivo temporal y el parámetro _lpszPrefix_ contiene los caracteres de prefijo del nombre de archivo. Es el nombre de archivo construido <prefix>HHHH. TMP, donde HHHH es un número hexadecimal. Si _lpszFileName_ es NULL, el archivo se creará en el directorio de archivos temporales que se devuelve desde la función de Windows **GetTempPath**o el directorio actual si no se ha designado ningún directorio de archivos temporales. 
  
Si no está establecido el indicador SOF_UNIQUEFILENAME, se omite _lpszPrefix_ y _lpszFileName_ debe contener la ruta de acceso completa y el nombre del archivo que se va a abrir o crear. El archivo se va a abrir o crear en función de los otros marcadores que se establecen en _ulFlags_. 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**File**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|File.cpp  <br/> |WriteAttachStreamToFile  <br/> |MFCMAPI usa el método **OpenStreamOnFile** para abrir un objeto stream en un archivo, por lo que se puede escribir un archivo adjunto a ella.  <br/> |
   
## <a name="see-also"></a>Vea también



[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

