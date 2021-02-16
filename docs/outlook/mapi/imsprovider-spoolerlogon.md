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

## <a name="parameters"></a>Parámetros

 _lpMAPISup_
  
> [entrada] Puntero al objeto de soporte MAPI para el almacén de mensajes.
    
 _ulUIParam_
  
> [entrada] Identificador de la ventana primaria de cualquier cuadro de diálogo o ventana que muestra este método. 
    
 _lpszProfileName_
  
> [entrada] Puntero a una cadena que contiene el nombre del perfil que se usa para el inicio de sesión de cola MAPI. Esta cadena puede mostrarse en cuadros de diálogo, escribirse en un archivo de registro o simplemente omitirse. Debe estar en formato Unicode si la marca MAPI_UNICODE está establecida en el _parámetro ulFlags._ 
    
 _cbEntryID_
  
> [entrada] Tamaño, en bytes, del identificador de entrada al que apunta el _parámetro lpEntryID._ 
    
 _lpEntryID_
  
> [entrada] Puntero al identificador de entrada del almacén de mensajes. Pasar NULL en el parámetro  _lpEntryID_ indica que aún no se ha seleccionado un almacén de mensajes y que se pueden presentar los cuadros de diálogo que permiten al usuario seleccionar un almacén de mensajes. 
    
 _ulFlags_
  
> [entrada] Máscara de bits de marcas que controla cómo se realiza el inicio de sesión. Se pueden establecer las siguientes marcas:
    
MAPI_DEFERRED_ERRORS 
  
> La llamada puede ser correcta incluso si el objeto subyacente no está disponible para la implementación de llamada. Si el objeto no está disponible, una llamada posterior al objeto podría generar un error.
    
MAPI_UNICODE 
  
> Las cadenas pasadas están en formato Unicode. Si MAPI_UNICODE no se establece, las cadenas están en formato ANSI.
    
MDB_NO_DIALOG 
  
> Impide que se muestren cuadros de diálogo de inicio de sesión. Si se establece esta marca, se devuelve el valor MAPI_E_LOGON_FAILED error si el inicio de sesión no se realiza correctamente. Si no se establece esta marca, el proveedor del almacén de mensajes puede pedir al usuario que corrija un nombre o contraseña, que inserte un disco o que realice otras acciones necesarias para establecer una conexión con el almacén.
    
MDB_WRITE 
  
> Solicita permiso de lectura y escritura.
    
 _lpInterface_
  
> [entrada] Puntero al identificador de interfaz (IID) en el que se debe iniciar sesión en el almacén de mensajes. Pasar NULL indica que se devuelve la interfaz MAPI para el almacén de mensajes ([IMsgStore](imsgstoreimapiprop.md)). El  _parámetro lpInterface_ también se puede establecer en un identificador para una interfaz adecuada para el almacén de mensajes (por ejemplo, IID_IUnknown o IID_IMAPIProp). 
    
 _cbSpoolSecurity_
  
> [entrada] Puntero al tamaño, en bytes, de los datos de validación en el parámetro _lppbSpoolSecurity._ 
    
 _lpbSpoolSecurity_
  
> [entrada] Puntero a un puntero a datos de validación. El **método SpoolerLogon** usa estos datos para iniciar sesión en la cola MAPI en el mismo almacén en el que el proveedor del almacén de mensajes inició sesión anteriormente mediante el método [IMSProvider::Logon.](imsprovider-logon.md) 
    
 _lppMAPIError_
  
> [salida] Puntero a un puntero a la estructura [MAPIERROR](mapierror.md) devuelta, si existe, que contiene información de versión, componente y contexto de un error. El  _parámetro lppMAPIError_ se puede establecer en NULL si no hay ninguna **estructura MAPIERROR** que devolver. 
    
 _lppMSLogon_
  
> [salida] Puntero al puntero al objeto de inicio de sesión del almacén de mensajes para que MAPI inicie sesión.
    
 _lppMDB_
  
> [salida] Puntero al puntero al objeto de almacén de mensajes para que la cola MAPI y las aplicaciones cliente inicien sesión.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
MAPI_E_UNCONFIGURED 
  
> El perfil no contiene información suficiente para que se complete el inicio de sesión. Cuando se devuelve este valor, MAPI llama a la función de punto de entrada del servicio de mensajes del proveedor del almacén de mensajes.
    
MAPI_W_ERRORS_RETURNED 
  
> La llamada se ha hecho correctamente, pero el proveedor del almacén de mensajes tiene información de error disponible. Cuando se devuelve esta advertencia, la llamada debe tratarse como correcta. Para probar esta advertencia, use la **macro HR_FAILED** datos. Para obtener más información, vea [Usar macros para el control de errores.](using-macros-for-error-handling.md) Para obtener la información de error del proveedor, llame al [método IMAPISession::GetLastError.](imapisession-getlasterror.md) 
    
## <a name="remarks"></a>Comentarios

La cola MAPI llama al método **IMSProvider::SpoolerLogon** para iniciar sesión en un almacén de mensajes. La cola MAPI debe usar el objeto de almacén de mensajes devuelto por el proveedor de al almacenamiento de mensajes en el parámetro  _lppMDB_ durante y después del inicio de sesión. 
  
Por coherencia con el [método IMSProvider::Logon,](imsprovider-logon.md) el proveedor también devuelve un objeto de inicio de sesión del almacén de mensajes en el parámetro _lppMSLogon._ El uso del objeto de almacén y el objeto de inicio de sesión son idénticos para el inicio de sesión habitual del almacén; debe haber una correspondencia uno a uno entre el objeto de inicio de sesión y el objeto de almacén, de forma que los objetos actúen como si fuera un objeto que exponga dos interfaces. Los dos objetos se crean juntos y se liberan juntos. 
  
El proveedor de almacenamiento debe marcar internamente el objeto de almacén de mensajes devuelto para indicar que la cola MAPI está utilizando el almacén. Algunos de los métodos para este objeto de almacén se comportan de forma diferente que para el objeto de almacén de mensajes proporcionado a las aplicaciones cliente. Mantener esta marca interna es la forma más común de desencadenar el comportamiento específico de la cola MAPI.
  
## <a name="see-also"></a>Consulte también



[IMSProvider::Logon](imsprovider-logon.md)
  
[MAPIERROR](mapierror.md)
  
[IMSProvider : IUnknown](imsprovideriunknown.md)

