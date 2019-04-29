---
title: IMSProviderSpoolerLogon
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSProvider.SpoolerLogon
api_type:
- COM
ms.assetid: 79d5af23-efad-4013-a330-56babfb2bb0f
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 794674df38266743cac8c947ec93dc1fcfff438b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430577"
---
# <a name="imsproviderspoolerlogon"></a>IMSProvider::SpoolerLogon

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Registra la cola MAPI en un almacén de mensajes.
  
```cpp
HRESULT SpoolerLogon(
  LPMAPISUP lpMAPISup,
  ULONG_PTR ulUIParam,
  LPSTR lpszProfileName,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulFlags,
  LPCIID lpInterface,
  ULONG cbSpoolSecurity,
  LPBYTE lpbSpoolSecurity,
  LPMAPIERROR FAR * lppMAPIError,
  LPMSLOGON FAR * lppMSLogon,
  LPMDB FAR * lppMDB     
);
```

## <a name="parameters"></a>Parameters

 _lpMAPISup_
  
> a Un puntero al objeto compatible con MAPI para el almacén de mensajes.
    
 _ulUIParam_
  
> a Un controlador para la ventana primaria de los cuadros de diálogo o ventanas que este método muestra. 
    
 _lpszProfileName_
  
> a Un puntero a una cadena que contiene el nombre del perfil que se usa para el inicio de sesión de la cola MAPI. Esta cadena se puede mostrar en cuadros de diálogo, se escribe en un archivo de registro o simplemente se pasa por alto. Debe estar en formato Unicode si la marca MAPI_UNICODE se establece en el parámetro _ulFlags_ . 
    
 _cbEntryID_
  
> a Tamaño, en bytes, del identificador de entrada al que apunta el parámetro _lpEntryID_ . 
    
 _lpEntryID_
  
> a Un puntero al identificador de entrada para el almacén de mensajes. Pasar NULL en el parámetro _lpEntryID_ indica que no se ha seleccionado todavía un almacén de mensajes y que se pueden presentar los cuadros de diálogo que permiten al usuario seleccionar un almacén de mensajes. 
    
 _ulFlags_
  
> a Una máscara de máscara de marcadores que controla cómo se realiza el inicio de sesión. Se pueden establecer los siguientes indicadores:
    
MAPI_DEFERRED_ERRORS 
  
> La llamada puede tener éxito incluso si el objeto subyacente no está disponible para la implementación que realiza la llamada. Si el objeto no está disponible, una llamada subsiguiente al objeto puede generar un error.
    
MAPI_UNICODE 
  
> Las cadenas pasadas están en formato Unicode. Si no se establece MAPI_UNICODE, las cadenas están en formato ANSI.
    
MDB_NO_DIALOG 
  
> Impide que se muestren los cuadros de diálogo de inicio de sesión. Si se establece esta marca, se devuelve el valor de error MAPI_E_LOGON_FAILED si el inicio de sesión no se ha realizado correctamente. Si no se establece esta marca, el proveedor de almacenamiento de mensajes puede pedir al usuario que corrija un nombre o contraseña, inserte un disco o realice otras acciones necesarias para establecer la conexión con el almacén.
    
MDB_WRITE 
  
> Solicita el permiso de lectura y escritura.
    
 _lpInterface_
  
> a Un puntero al identificador de interfaz (IID) del almacén de mensajes en el que se va a iniciar sesión. Pasar NULL indica que se devuelve la interfaz MAPI para el almacén de mensajes ([IMsgStore](imsgstoreimapiprop.md)). El parámetro _lpInterface_ también se puede establecer en un identificador para una interfaz adecuada para el almacén de mensajes (por ejemplo, IID_IUnknown o IID_IMAPIProp). 
    
 _cbSpoolSecurity_
  
> a Puntero al tamaño, en bytes, de los datos de validación en el parámetro _lppbSpoolSecurity_ . 
    
 _lpbSpoolSecurity_
  
> a Un puntero a un puntero a datos de validación. El método **SpoolerLogon** usa estos datos para registrar la cola MAPI en el mismo almacén en el que el proveedor de almacenamiento de mensajes inició sesión previamente mediante el método [IMSProvider:: Logon](imsprovider-logon.md) . 
    
 _lppMAPIError_
  
> contempla Un puntero a un puntero a la estructura [MAPIERROR](mapierror.md) devuelta, si existe, que contiene información de la versión, el componente y el contexto de un error. El parámetro _lppMAPIError_ puede establecerse en NULL si no hay ninguna estructura **MAPIERROR** para devolver. 
    
 _lppMSLogon_
  
> contempla Un puntero al puntero al objeto de inicio de sesión de un almacén de mensajes para que MAPI inicie sesión.
    
 _lppMDB_
  
> contempla Un puntero al puntero al objeto de almacén de mensajes para la cola MAPI y las aplicaciones cliente en las que se va a iniciar sesión.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
MAPI_E_UNCONFIGURED 
  
> El perfil no contiene suficiente información para que el inicio de sesión se complete. Cuando se devuelve este valor, MAPI llama a la función de punto de entrada del servicio de mensajes del proveedor de almacenamiento de mensajes.
    
MAPI_W_ERRORS_RETURNED 
  
> La llamada se realizó correctamente, pero el proveedor de almacenamiento de mensajes tiene información de error disponible. Cuando se devuelve esta advertencia, la llamada se debe administrar como correcta. Para probar esta advertencia, use la macro **HR_FAILED** . Para obtener más información, consulte [usar macros para el control de errores](using-macros-for-error-handling.md). Para obtener la información de error del proveedor, llame al método [IMAPISession:: GetLastError](imapisession-getlasterror.md) . 
    
## <a name="remarks"></a>Comentarios

La cola MAPI llama al método **IMSProvider:: SpoolerLogon** para iniciar sesión en un almacén de mensajes. La cola MAPI debe usar el objeto de almacén de mensajes devuelto por el proveedor de almacenamiento de mensajes en el parámetro _lppMDB_ durante y después del inicio de sesión. 
  
Por coherencia con el método [IMSProvider:: Logon](imsprovider-logon.md) , el proveedor también devuelve un objeto de inicio de sesión del almacén de mensajes en el parámetro _lppMSLogon_ . El uso del objeto Store y el objeto de inicio de sesión son idénticos para el inicio de sesión del almacén habitual; debe haber una correspondencia de uno a uno entre el objeto de inicio de sesión y el objeto de almacén de forma que los objetos actúen como si fueran un objeto que expone dos interfaces. Los dos objetos se crean y se liberan juntos. 
  
El proveedor de almacenamiento debe marcar internamente el objeto de almacén de mensajes devuelto para indicar que la cola de MAPI está usando el almacén. Algunos de los métodos para este objeto Store se comportan de forma diferente que para el objeto de almacén de mensajes proporcionado a las aplicaciones cliente. Mantener esta marca interna es la forma más común de desencadenar el comportamiento específico de la cola MAPI.
  
## <a name="see-also"></a>Ver también



[IMSProvider::Logon](imsprovider-logon.md)
  
[MAPIERROR](mapierror.md)
  
[IMSProvider : IUnknown](imsprovideriunknown.md)

