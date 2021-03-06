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
  
> [in] Puntero al objeto de soporte mapi para el almacén de mensajes.
    
 _ulUIParam_
  
> [in] Un identificador de la ventana principal de cualquier cuadro de diálogo o ventana que muestre este método. 
    
 _lpszProfileName_
  
> [in] Puntero a una cadena que contiene el nombre del perfil que se va a usar para el inicio de sesión de cola MAPI. Esta cadena puede mostrarse en cuadros de diálogo, escribirse en un archivo de registro o simplemente omitirse. Debe estar en formato Unicode si la MAPI_UNICODE se establece en el _parámetro ulFlags._ 
    
 _cbEntryID_
  
> [in] Tamaño, en bytes, del identificador de entrada al que apunta el _parámetro lpEntryID._ 
    
 _lpEntryID_
  
> [in] Puntero al identificador de entrada del almacén de mensajes. Pasar NULL en el parámetro  _lpEntryID_ indica que aún no se ha seleccionado un almacén de mensajes y que se pueden presentar cuadros de diálogo que permiten al usuario seleccionar un almacén de mensajes. 
    
 _ulFlags_
  
> [in] Máscara de bits de marcas que controla cómo se realiza el inicio de sesión. Se pueden establecer las siguientes marcas:
    
MAPI_DEFERRED_ERRORS 
  
> La llamada puede tener éxito incluso si el objeto subyacente no está disponible para la implementación de llamada. Si el objeto no está disponible, una llamada posterior al objeto podría generar un error.
    
MAPI_UNICODE 
  
> Las cadenas pasadas están en formato Unicode. Si MAPI_UNICODE no está establecido, las cadenas tienen el formato ANSI.
    
MDB_NO_DIALOG 
  
> Impide la presentación de cuadros de diálogo de inicio de sesión. Si se establece esta marca, el valor de error MAPI_E_LOGON_FAILED se devuelve si el inicio de sesión no se realiza correctamente. Si no se establece esta marca, el proveedor del almacén de mensajes puede solicitar al usuario que corrija un nombre o contraseña, inserte un disco o realice otras acciones necesarias para establecer la conexión al almacén.
    
MDB_WRITE 
  
> Solicitudes de permiso de lectura y escritura.
    
 _lpInterface_
  
> [in] Puntero al identificador de interfaz (IID) para que el almacén de mensajes inicie sesión. Si se pasa NULL, se devuelve la interfaz MAPI del almacén de mensajes ([IMsgStore](imsgstoreimapiprop.md)). El  _parámetro lpInterface_ también se puede establecer en un identificador para una interfaz adecuada para el almacén de mensajes (por ejemplo, IID_IUnknown o IID_IMAPIProp). 
    
 _cbSpoolSecurity_
  
> [in] Puntero al tamaño, en bytes, de los datos de validación en el _parámetro lppbSpoolSecurity._ 
    
 _lpbSpoolSecurity_
  
> [in] Puntero a un puntero a datos de validación. El **método SpoolerLogon** usa estos datos para registrar la cola MAPI en el mismo almacén que el proveedor del almacén de mensajes que inició sesión anteriormente mediante el método [IMSProvider::Logon.](imsprovider-logon.md) 
    
 _lppMAPIError_
  
> [salida] Puntero a un puntero a la estructura [MAPIERROR](mapierror.md) devuelta, si la hubiera, que contiene información de versión, componente y contexto de un error. El  _parámetro lppMAPIError_ se puede establecer en NULL si no hay ninguna **estructura MAPIERROR** que devolver. 
    
 _lppMSLogon_
  
> [salida] Puntero al puntero al objeto de inicio de sesión del almacén de mensajes para que MAPI inicie sesión.
    
 _lppMDB_
  
> [salida] Puntero al puntero al objeto de almacén de mensajes para que la cola MAPI y las aplicaciones cliente inicien sesión.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
MAPI_E_UNCONFIGURED 
  
> El perfil no contiene suficiente información para que se complete el inicio de sesión. Cuando se devuelve este valor, MAPI llama a la función de punto de entrada del servicio de mensajes del proveedor del almacén de mensajes.
    
MAPI_W_ERRORS_RETURNED 
  
> La llamada se ha hecho correctamente, pero el proveedor del almacén de mensajes tiene información de error disponible. Cuando se devuelve esta advertencia, la llamada debe controlarse como correcta. Para probar esta advertencia, use la **HR_FAILED** macro. Para obtener más información, vea [Using Macros for Error Handling](using-macros-for-error-handling.md). Para obtener la información de error del proveedor, llame al [método IMAPISession::GetLastError.](imapisession-getlasterror.md) 
    
## <a name="remarks"></a>Comentarios

La cola MAPI llama al método **IMSProvider::SpoolerLogon** para iniciar sesión en un almacén de mensajes. La cola MAPI debe usar el objeto de almacén de mensajes devuelto por el proveedor del almacén de mensajes en el parámetro  _lppMDB_ durante y después del inicio de sesión. 
  
Por coherencia con el [método IMSProvider::Logon,](imsprovider-logon.md) el proveedor también devuelve un objeto de inicio de sesión de almacén de mensajes en el _parámetro lppMSLogon._ El uso del objeto store y el objeto de inicio de sesión son idénticos para el inicio de sesión habitual del almacén; debe haber una correspondencia uno a uno entre el objeto de inicio de sesión y el objeto store de manera que los objetos actúen como si se trata de un objeto que exponga dos interfaces. Los dos objetos se crean juntos y se liberan juntos. 
  
El proveedor de almacenamiento debe marcar internamente el objeto de almacén de mensajes devuelto para indicar que la cola MAPI está utilizando el almacén. Algunos de los métodos de este objeto de almacén se comportan de forma diferente que para el objeto de almacén de mensajes proporcionado a las aplicaciones cliente. Mantener esta marca interna es la forma más común de desencadenar el comportamiento específico de la cola MAPI.
  
## <a name="see-also"></a>Vea también



[IMSProvider::Logon](imsprovider-logon.md)
  
[MAPIERROR](mapierror.md)
  
[IMSProvider : IUnknown](imsprovideriunknown.md)

