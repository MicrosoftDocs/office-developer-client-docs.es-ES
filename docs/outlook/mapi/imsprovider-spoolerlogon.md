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
ms.openlocfilehash: eaf84e1b2a747b313f1534eb66b190d86cf89df9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817820"
---
# <a name="imsproviderspoolerlogon"></a>IMSProvider::SpoolerLogon

  
  
**Hace referencia a**: Outlook 
  
Inicie sesión en un almacén de mensajes en la cola de MAPI.
  
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
  
> [entrada] Un puntero a la interfaz MAPI admite el objeto para el almacén de mensajes.
    
 _ulUIParam_
  
> [entrada] Un identificador de la ventana principal de windows o cuadros de diálogo que muestra este método. 
    
 _lpszProfileName_
  
> [entrada] Un puntero a una cadena que contiene el nombre del perfil que se utiliza para el inicio de sesión de cola de impresión MAPI. Esta cadena se puede que se muestra en los cuadros de diálogo, escriben en un archivo de registro o simplemente se omite. Debe estar en formato Unicode si está establecido el indicador MAPI_UNICODE en el parámetro _ulFlags indicado_ . 
    
 _cbEntryID_
  
> [entrada] El tamaño, en bytes, del identificador de entrada indicada por el parámetro _lpEntryID_ . 
    
 _lpEntryID_
  
> [entrada] Un puntero al identificador de entrada para el almacén de mensajes. Pasar NULL en el parámetro _lpEntryID_ indica que no se ha seleccionado aún un almacén de mensajes y que se pueden presentar cuadros de diálogo que permiten al usuario seleccionar un almacén de mensajes. 
    
 _ulFlags_
  
> [entrada] Una máscara de bits de indicadores que controla cómo se realiza el inicio de sesión. Se pueden establecer los siguientes indicadores:
    
MAPI_DEFERRED_ERRORS 
  
> Se autoriza la llamada se realice correctamente, incluso si el objeto subyacente no está disponible para la implementación de la llamada. Si el objeto no está disponible, una llamada posterior al objeto podría provocar un error.
    
MAPI_UNICODE. 
  
> Las cadenas que se pasan en están en formato Unicode. Si no se establece MAPI_UNICODE., las cadenas están en formato ANSI.
    
MDB_NO_DIALOG 
  
> Impide la presentación de cuadros de diálogo de inicio de sesión. Si se establece este marcador, se devuelve el valor de error MAPI_E_LOGON_FAILED si el inicio de sesión se realiza correctamente. Si no se establece este indicador, el proveedor de almacenamiento de mensaje puede solicitar al usuario para corregir un nombre o una contraseña, para insertar un disco, o para llevar a cabo otras acciones necesarias para establecer la conexión con el almacén.
    
MDB_WRITE 
  
> Las solicitudes de permiso de lectura y escritura.
    
 _lpInterface_
  
> [entrada] Un puntero para el identificador de interfaz (IID) para iniciar sesión en el almacén de mensajes. Paso de NULL indica que se devuelve la interfaz de MAPI para el almacén de mensajes ([IMsgStore](imsgstoreimapiprop.md)). El parámetro _lpInterface_ también se puede establecer en un identificador para una interfaz adecuada para el almacén de mensajes (por ejemplo IID_IUnknown o IID_IMAPIProp). 
    
 _cbSpoolSecurity_
  
> [entrada] Un puntero al tamaño, en bytes, de los datos de validación en el parámetro _lppbSpoolSecurity_ . 
    
 _lpbSpoolSecurity_
  
> [entrada] Un puntero a un puntero a los datos de validación. El método **SpoolerLogon** utiliza estos datos para iniciar sesión en el mismo almacén de la cola de MAPI como el proveedor de almacenamiento de mensaje que inició sesión anteriormente en mediante el método [IMSProvider::Logon](imsprovider-logon.md) . 
    
 _lppMAPIError_
  
> [out] Un puntero a un puntero a la [MAPIERROR](mapierror.md) estructura devuelta, si lo hay, que contiene información de versión, el componente y el contexto de un error. El parámetro _lppMAPIError_ se puede establecer en NULL si no hay ninguna estructura **MAPIERROR** para devolver. 
    
 _lppMSLogon_
  
> [out] Un puntero al puntero para el mensaje almacena el objeto de inicio de sesión de MAPI iniciar sesión en.
    
 _lppMDB_
  
> [out] Un puntero al puntero para el mensaje almacena el objeto de la cola MAPI y las aplicaciones de cliente para iniciar sesión en.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
MAPI_E_UNCONFIGURED 
  
> El perfil no contiene información suficiente para el inicio de sesión para llevar a cabo. Cuando se devuelve este valor, MAPI llama la función de punto de entrada de servicio de mensajes del proveedor de almacén de mensajes.
    
MAPI_W_ERRORS_RETURNED 
  
> La llamada se ha realizado correctamente, pero el proveedor de almacén de mensajes tiene información de error disponible. Cuando se devuelve esta advertencia, la llamada se debe controlarse como correcta. Para probar esta advertencia, utilice la macro **HR_FAILED** . Para obtener más información, vea [Uso de Macros para el control de errores](using-macros-for-error-handling.md). Para obtener la información de error desde el proveedor, llame al método [IMAPISession::GetLastError](imapisession-getlasterror.md) . 
    
## <a name="remarks"></a>Comentarios

La cola MAPI llama al método de **IMSProvider::SpoolerLogon** para iniciar sesión en un almacén de mensajes. La cola MAPI debe usar el objeto de almacén de mensaje devuelto por el proveedor de almacén de mensajes en el parámetro _lppMDB_ durante y después de inicio de sesión. 
  
Para mantener la coherencia con el método [IMSProvider::Logon](imsprovider-logon.md) , el proveedor también devuelve un objeto de inicio de sesión del almacén de mensajes en el parámetro _lppMSLogon_ . El uso del objeto de almacenamiento y el objeto de inicio de sesión son idénticos para inicio de sesión de almacenamiento habitual; debe haber una correspondencia uno a uno entre el objeto de inicio de sesión y el objeto de almacén de manera que los objetos que actúe como si fueran un único objeto que expone dos interfaces. Los dos objetos se crean juntos y liberado juntos. 
  
El proveedor de almacenamiento debe marcar internamente el objeto de almacén de mensaje devuelto para indicar que se está utilizando el almacén de la cola de MAPI. Algunos de los métodos de este objeto de almacenamiento se comportan de forma diferente para el mensaje de almacenar el objeto proporcionado a las aplicaciones cliente. Mantener esta marca interna es la manera más común de desencadenar el comportamiento específico de la cola de MAPI.
  
## <a name="see-also"></a>Vea también



[IMSProvider::Logon](imsprovider-logon.md)
  
[MAPIERROR](mapierror.md)
  
[IMSProvider : IUnknown](imsprovideriunknown.md)

