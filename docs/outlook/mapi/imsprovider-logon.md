---
title: IMSProviderLogon
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSProvider.Logon
api_type:
- COM
ms.assetid: 890d9cbe-3570-4cf0-aeae-667c0e5ba181
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: b89c8129f68852bdd243a7f984497ab312aa2551
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817833"
---
# <a name="imsproviderlogon"></a>IMSProvider::Logon

  
  
**Hace referencia a**: Outlook 
  
Registros MAPI sesión en una instancia de un proveedor de almacén de mensajes.
  
```cpp
HRESULT Logon(
  LPMAPISUP lpMAPISup,
  ULONG_PTR ulUIParam,
  LPSTR lpszProfileName,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulFlags,
  LPCIID lpInterface,
  ULONG FAR * lpcbSpoolSecurity,
  LPBYTE FAR * lppbSpoolSecurity,
  LPMAPIERROR FAR * lppMAPIError,
  LPMSLOGON FAR * lppMSLogon,
  LPMDB FAR * lppMDB
);
```

## <a name="parameters"></a>Parámetros

 _lpMAPISup_
  
> [entrada] Un puntero a la interfaz MAPI actual admite el objeto para el almacén de mensajes.
    
 _ulUIParam_
  
> [entrada] Un identificador de la ventana principal de windows o cuadros de diálogo que muestra este método. 
    
 _lpszProfileName_
  
> [entrada] Un puntero a una cadena que contiene el nombre del perfil que se utiliza para el inicio de sesión de proveedor de almacén. Esta cadena se puede que se muestra en los cuadros de diálogo, escriben en un archivo de registro o simplemente se omite. Debe estar en formato Unicode si está establecido el indicador MAPI_UNICODE en el parámetro _ulFlags indicado_ . 
    
 _cbEntryID_
  
> [entrada] El tamaño, en bytes, del identificador de entrada indicada por el parámetro _lpEntryID_ . 
    
 _lpEntryID_
  
> [entrada] Un puntero al identificador de entrada para el almacén de mensajes. Pasar **null** en _lpEntryID_ indica que no se ha seleccionado aún un almacén de mensajes y que se pueden presentar cuadros de diálogo que permiten al usuario seleccionar un almacén de mensajes. 
    
 _ulFlags_
  
> [entrada] Una máscara de bits de indicadores que controla cómo se realiza el inicio de sesión. Se pueden establecer los siguientes indicadores:
    
MAPI_DEFERRED_ERRORS 
  
> Se autoriza la llamada se realice correctamente, incluso si el objeto subyacente no está disponible para la implementación de la llamada. Si el objeto no está disponible, una llamada posterior al objeto podría provocar un error.
    
MAPI_UNICODE. 
  
> Las cadenas que se pasan en están en formato Unicode. Si no se establece MAPI_UNICODE., las cadenas están en formato ANSI.
    
MDB_NO_DIALOG 
  
> Impide la presentación de cuadros de diálogo de inicio de sesión. Si se establece este marcador, se devuelve el valor de error MAPI_E_LOGON_FAILED si el inicio de sesión se realiza correctamente. Si no se establece este indicador, el proveedor de almacenamiento de mensaje puede solicitar al usuario para corregir un nombre o una contraseña, para insertar un disco, o para llevar a cabo otras acciones que son necesarias para establecer la conexión con el almacén.
    
MDB_NO_MAIL 
  
> El almacén de mensajes no debe usarse para enviar o recibir correo. La marca de señales de MAPI no para notificar a la cola MAPI que se va a abrir este almacén de mensajes. Si se establece este indicador y el almacén de mensajes se complementa con un proveedor de transporte, el proveedor no es necesario llamar al método [SpoolerNotify](imapisupport-spoolernotify.md) . 
    
MDB_TEMPORARY 
  
> Los registros en el almacén de modo que la información se puede recuperar mediante programación en la sección de perfil, sin el uso de cuadros de diálogo. Esta marca indica a MAPI, que es el almacén no que se agregarán a la tabla de almacén de mensajes y que el almacén no se pueden hacer permanente. Si se establece este marcador, los proveedores de almacén de mensajes no es necesario llamar al método [IMAPISupport::ModifyProfile](imapisupport-modifyprofile.md) . 
    
MDB_WRITE 
  
> Las solicitudes de permiso de lectura y escritura.
    
 _lpInterface_
  
> [entrada] Un puntero para el identificador de interfaz (IID) para iniciar sesión en el almacén de mensajes. Si se pasa **null** indica que se devuelve la interfaz de MAPI para el almacén de mensajes ( [IMsgStore](imsgstoreimapiprop.md)). El parámetro _lpInterface_ también se puede establecer en un identificador para una interfaz adecuada para el almacén de mensajes (por ejemplo, IID_IUnknown o IID_IMAPIProp). 
    
 _lpcbSpoolSecurity_
  
> [out] Un puntero a la variable en el que el proveedor de almacenamiento devuelve el tamaño, en bytes, de los datos de validación en el parámetro _lppbSpoolSecurity_ . 
    
 _lppbSpoolSecurity_
  
> [out] Un puntero al puntero a los datos de validación devuelto. Esta validación de datos se proporciona para que el método [IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md) puede iniciar sesión en el mismo almacén de la cola de MAPI como el proveedor de almacén de mensajes. 
    
 _lppMAPIError_
  
> [out] Un puntero a un puntero a la [MAPIERROR](mapierror.md) estructura devuelta, si lo hay, que contiene información de versión, el componente y el contexto de un error. El parámetro _lppMAPIError_ se puede establecer en **null** si no hay ninguna estructura **MAPIERROR** para devolver. 
    
 _lppMSLogon_
  
> [out] Un puntero al puntero para el mensaje almacena el objeto de inicio de sesión de MAPI iniciar sesión en.
    
 _lppMDB_
  
> [out] Un puntero al puntero para el mensaje almacena el objeto de la cola MAPI y las aplicaciones de cliente para iniciar sesión en.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
MAPI_E_FAILONEPROVIDER 
  
> Este proveedor no puede iniciar sesión, pero este error debe deshabilitar el servicio. 
    
MAPI_E_LOGON_FAILED 
  
> No se pudo establecer una sesión de inicio de sesión.
    
MAPI_E_UNCONFIGURED 
  
> El perfil no contiene información suficiente para el inicio de sesión para llevar a cabo. Cuando se devuelve este valor, MAPI llama la función de punto de entrada del servicio de mensajes del proveedor de almacén de mensajes.
    
MAPI_E_USER_CANCEL 
  
> El usuario canceló la operación, normalmente haciendo clic en el botón **Cancelar** en un cuadro de diálogo. 
    
MAPI_E_UNKNOWN_CPID 
  
> El servidor no está configurado para admitir la página de códigos del cliente.
    
MAPI_E_UNKNOWN_LCID 
  
> El servidor no está configurado para admitir la información de configuración regional del cliente.
    
MAPI_W_ERRORS_RETURNED 
  
> La llamada se ha realizado correctamente, pero el proveedor de almacén de mensajes tiene información de error disponible. Cuando se devuelve esta advertencia, la llamada se debe controlarse como correcta. Para probar esta advertencia, utilice la macro **HR_FAILED** . Para obtener más información, vea [Uso de Macros para el control de errores](using-macros-for-error-handling.md). Para obtener la información de error desde el proveedor, llame al método [IMAPISession::GetLastError](imapisession-getlasterror.md) . 
    
## <a name="remarks"></a>Comentarios

MAPI llama el método **IMSProvider::Logon** para llevar a cabo la mayoría de los procesos necesarios para obtener acceso a un almacén de mensajes. Los proveedores de almacén de mensajes validar cualquier las credenciales de usuario necesarias para tener acceso a un almacén determinado y devolver un objeto de almacén de mensajes en el parámetro _lppMDB_ que las aplicaciones de cliente y de la cola de impresión MAPI pueden iniciar sesión en. 
  
Además del objeto de almacén de mensaje devuelto para el cliente y el uso de la cola de impresión MAPI, el proveedor también devuelve un objeto de inicio de sesión del almacén de mensajes de MAPI usar en el control de la tienda abierta. El objeto de inicio de sesión del almacén de mensajes y el objeto de almacén de mensajes deben vincularse estrechamente dentro del proveedor de almacén de mensajes para cada uno de ellos puede afectar a la otra. El uso del objeto de almacenamiento y el objeto de inicio de sesión debe ser idéntico; debe haber una correspondencia uno a uno entre el objeto de inicio de sesión y el objeto de almacén de manera que los objetos que actúe como si fueran un único objeto que expone dos interfaces. Los dos objetos también se deben crear juntos y liberado juntos. 
  
El objeto compatible con MAPI, creado por MAPI y se pasan al proveedor en el parámetro _lpMAPISup_ , proporciona acceso a las funciones de MAPI que requiere el proveedor. Éstas incluyen las funciones que guardar y recuperar información de perfil, tener acceso a las libretas de direcciones y así sucesivamente. El puntero _lpMAPISup_ puede ser diferente para cada almacén que se abre. Mientras el procesamiento llama a un almacén de mensajes después de inicio de sesión, el proveedor de almacenamiento debe usar la variable _lpMAPISup_ que es específica de ese almacén. Para cualquier llamada de **Inicio de sesión** que se abre un almacén de mensajes y funciona correctamente en la creación de un objeto de inicio de sesión del almacén de mensajes, el proveedor debe guardar un puntero al objeto de compatibilidad con MAPI en el objeto de inicio de sesión de almacén y debe llamar al método [IUnknown:: AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28v=VS.85%29.aspx) para agregar una referencia para el objeto de soporte. 
  
El parámetro _ulUIParam_ debe usarse si el proveedor presenta cuadros de diálogo durante la llamada de **Inicio de sesión** . Sin embargo, cuadros de diálogo no deben presentarse si _ulFlags_ contiene la marca MDB_NO_DIALOG. Si necesita una interfaz de usuario que se llame pero _ulFlags_ no permitir, o si por alguna otra razón no se puede mostrar una interfaz de usuario, el proveedor debe devolver MAPI_E_LOGON_FAILED. Si el **Inicio de sesión** muestra un cuadro de diálogo y el usuario cancela el inicio de sesión, normalmente haciendo clic en el botón **Cancelar** del cuadro de diálogo, el proveedor debe devolver MAPI_E_USER_CANCEL. 
  
El parámetro _lpEntryID_ puede ser **null** o elija un identificador de entrada no ajustado almacén que almacenar este mensaje creado anteriormente. Si _lpEntryID_ señala a un identificador de entrada no ajustado, ese identificador de entrada puede proceder de uno de varios lugares: 
  
- Puede ser un identificador de entrada que el proveedor de almacenamiento anteriormente ajustado y se escribió en la sección de perfil como una propiedad de **entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md)).
    
- Puede ser un identificador de entrada que el proveedor anteriormente ajustado y vuelvan a un cliente de la llamada como una propiedad de **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)). 
    
- Puede ser un identificador de entrada que el proveedor anteriormente ajustado y vuelvan a un cliente de la llamada como la propiedad de **entrada del objeto** de un objeto de almacén de mensajes. 
    
En cualquiera de estos casos, es posible que el identificador de entrada se ha creado en un equipo diferente del que usa actualmente.
  
Cuando _lpEntryID_ no es **nulo**, debe contener toda la información necesaria para identificar y busque el almacén de mensajes. Esta información puede incluir los nombres de volumen de red, los números de teléfono, nombres de cuenta de usuario y así sucesivamente. Si la conexión con el almacén no puede realizarse mediante el uso de los datos en el identificador de entrada, el proveedor de almacenamiento debe mostrar un cuadro de diálogo que permite al usuario seleccionar el almacén que se va a abrir. Un cuadro de diálogo puede ser necesario, por ejemplo, si se ha cambiado el nombre de un servidor, un nombre de cuenta ha cambiado o partes de la red no están disponibles.
  
Cuando _lpEntryID_ es **null**, se que aún no se ha seleccionado el almacén de mensajes para usar. El proveedor aún puede tener acceso a un almacén sin mostrar un cuadro de diálogo si es compatible con otros métodos para especificar el almacén. Por ejemplo, el proveedor puede comprobar su archivo de inicialización o que puede buscar las propiedades adicionales que se colocaron en la sección de perfil de su o su mensaje del servicio en la configuración.
  
Si un proveedor busca todas la información necesaria no está en el perfil, debe devolver MAPI_E_UNCONFIGURED. MAPI le llamará en función del punto de entrada del proveedor mensaje servicio para permitir que el usuario para seleccionar un almacén, o incluso para crear uno, y escribir un nombre de cuenta y una contraseña, como sea necesario. MAPI crea automáticamente una nueva sección de perfil para un nuevo almacén; en esta sección de perfil nuevo puede ser temporal o permanente, dependiendo de cómo se ha agregado. Si el proveedor de almacenamiento llama al método de **IMAPISupport::ModifyProfile** , la nueva sección de perfil se convierte en permanente y el almacén se agrega a la lista de almacenes de mensaje devuelto por el método [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) . 
  
El parámetro _lpInterface_ especifica el IID de la interfaz necesaria para el objeto store acaba de abrir. Pasar **null** en _lpInterface_ especifica que la interfaz de almacén de mensajes MAPI, **IMsgStore**, es necesaria. Pase el objeto de almacén de mensajes, IID_IMsgStore, también especifica que se requiere **IMsgStore** . Si se pasa IID_IUnknown en _lpInterface_, el proveedor debe abrir el almacén de mediante el uso de cualquier interfaz derivada de [IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28v=VS.85%29.aspx) es mejor para el proveedor (de nuevo, esto es normalmente **IMsgStore**). Cuando se pasa IID_IUnknown, la implementación llamada usa el método [IUnknown:: QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx) para seleccionar una interfaz después de que se haya realizado correctamente la operación de apertura de almacén. 
  
La llamada **IMSProvider::Logon** debe devolver información suficiente, como una ruta de acceso en el almacén y las credenciales para tener acceso al almacén, para permitir que la cola MAPI iniciar sesión en el mismo almacén que el proveedor de almacenamiento hace sin presentar un cuadro de diálogo. Los parámetros _lpcbSpoolSecurity_ y _lppbSpoolSecurity_ se utilizan para devolver esta información. El proveedor asigna la memoria para estos datos pasando un puntero a un búfer en [MSProviderInit](msproviderinit.md) _lpfAllocateBuffer_ parámetro de la función; el proveedor coloca el tamaño de este búfer en _lpcbSpoolSecurity_. 
  
MAPI libera este búfer cuando sea apropiado. Si el inicio de sesión de la cola MAPI en el almacén de puede realizarse de la información en la sección de perfil por sí solo, el proveedor puede devolver null en _lppbSpoolSecurity_ y 0 para el tamaño de la información en _lpcbSpoolSecurity_. El inicio de sesión de la cola MAPI se produce como parte de un proceso diferente que el inicio de sesión de almacén; debido a que el búfer que contiene la información pasada obtiene copiado entre procesos, podría no ser en la memoria en la misma ubicación para el proceso de cola de impresión MAPI que para el proceso de proveedor de almacén. Por lo tanto, un proveedor no debe poner las direcciones en este búfer. Para obtener más información sobre el inicio de sesión MAPI cola de impresión, vea el método [IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md) . 
  
La mayoría de los proveedores de almacén use el método [IMAPISession::OpenProfileSection](imapisession-openprofilesection.md) del objeto de soporte técnico pasado en el parámetro _lpMAPISup_ para guardar y recuperar las opciones y las credenciales de usuario. **OpenProfileSection** permite que un proveedor de almacenamiento guardar información arbitraria adicional en una sección de perfil y asociarlo a un recurso determinado. Por ejemplo, un proveedor de almacén puede guardar el nombre de la cuenta de usuario y la contraseña asociada a un recurso y las rutas de acceso u otra información necesaria para tener acceso a ese recurso. 
  
Las propiedades con identificadores de propiedad 0x6600 a través de 0x67FF son propiedades seguras disponibles para el proveedor para su propio uso almacenar datos privados en las secciones del perfil. Para obtener más información acerca de los usos de propiedades en los objetos de sección de perfil, vea el [IProfSect: IMAPIProp](iprofsectimapiprop.md) (método). 
  
Además de los datos privados de propiedades con identificadores de 0x6600 a través de 0x67FF, el proveedor de almacenamiento debe proporcionar información de la propiedad **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) en su sección de perfil. Debe colocar en **PR_DISPLAY_NAME** el nombre para mostrar del proveedor: una cadena de identificación (por ejemplo, "Microsoft Personal Information Store") que se muestra a los usuarios para que pueden distinguir este almacén de mensajes de otros usuarios es posible que tenga acceso Para. **PR_DISPLAY_NAME** normalmente contiene un nombre de servidor, el nombre de la cuenta de usuario o la ruta de acceso. 
  
Algunas propiedades de la sección de perfil están visibles en la tabla de almacén de mensajes; otros usuarios están visibles durante el programa de instalación, la instalación y la configuración del subsistema MAPI. Normalmente, el proveedor proporciona información para estas propiedades visibles para una nueva sección de perfil, que aún no incluye las credenciales guardadas o información privada y, cuando se encuentre que ha cambiado la información de la propiedad. Para obtener más información acerca de las secciones del perfil, vea [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md).
  
Después de iniciar sesión correctamente en un usuario y antes de volver a MAPI, el proveedor de almacenamiento debe crear la matriz de propiedades de la fila de estado para el recurso y llame al método [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) . 
  
 Las llamadas de **Inicio de sesión** que se abren los almacenes de mensajes que ya están abiertos para la sesión MAPI actual omitir gran parte del procesamiento descrito anteriormente. Estas llamadas no crear filas de estado, devolver objetos de inicio de sesión del almacén de mensajes, llamar a **AddRef** para el objeto de la compatibilidad con MAPI o devolver datos para el inicio de sesión MAPI cola de impresión. Estas llamadas devuelve S_OK y devolver un objeto de almacén de mensajes con la interfaz solicitada. 
  
Para detectar este tipo de llamadas, el proveedor debe mantener una lista en el objeto de proveedor de almacén de mensajes de almacenes ya está abierto para este objeto de proveedor. Cuando se procesa una llamada de **Inicio de sesión** , el proveedor debe analizar esta lista de almacenes de open y determinar si el almacén debe tener una sesión iniciada en ya está abierto. Si es así, las credenciales de usuario no es necesario que se va a comprobar y se debe evitar la presentación de un cuadro de diálogo, si es posible. Si se deben mostrar cuadros de diálogo, el proveedor debe comprobar la información devuelta para ver si un almacén se ha abierto una segunda vez. Además, debe comprobar el proveedor de aperturas duplicadas mediante _lpEntryID_ al principio de llamada de **Inicio de sesión** de procesamiento. 
  
Procesamiento de una llamada de **Inicio de sesión** que obtiene acceso a un almacén de open estándar es como sigue: 
  
1. El proveedor de almacenamiento llama a **AddRef** para el objeto de almacenamiento existente si la nueva interfaz que se solicita es el mismo que la interfaz para el almacén existente. De lo contrario, llama a **QueryInterface** para obtener la nueva interfaz. Si el almacén no es compatible con la nueva interfaz, el proveedor debe devolver el valor de error MAPI_E_INTERFACE_NOT_SUPPORTED. 
    
2. El proveedor devuelve un puntero a la interfaz necesaria del objeto de almacenamiento existente en _lppMDB_.
    
3. El proveedor devuelve **null** en _lppMSLogon_.
    
4. El proveedor no debe abrir el perfil para el objeto de soporte técnico que se pasa en la llamada. Además, no debe registrar un identificador único del proveedor, registrar una fila de estado o devolver datos de inicio de sesión de cola de MAPI.
    
5. El proveedor no debe llamar a **AddRef** para el objeto de soporte técnico, ya que no requiere un puntero al objeto. 
    
Siempre que sea posible, los proveedores deben devolver adecuado de error y advertencia cadenas para las llamadas de **Inicio de sesión** , porque si lo hace, en gran medida facilita la carga de usuarios en determinar por qué algo no funcionó. Para devolver estas cadenas, un proveedor establece a los miembros de la estructura de **MAPIERROR** . MAPI busca, utiliza y libera la estructura **MAPIERROR** si es devuelto por un proveedor. 
  
Memoria de esta estructura **MAPIERROR** debe asignarse usando el búfer pasado en _lpfAllocateBuffer_ en la llamada **MSProviderInit** . Cualquier error en las cadenas contenidas en la estructura devuelta deben estar en formato Unicode si MAPI_UNICODE se establece en el **Inicio de sesión** _ulFlags;_ en caso contrario, se debe en el carácter ANSI establecer. 
  
Para la mayoría de los valores de error devuelta desde el **Inicio de sesión**, MAPI deshabilita los servicios de mensaje a la que pertenece el proveedor con errores. MAPI no llamará a todos los proveedores que pertenecen a esos servicios durante la vida de la sesión MAPI. Por el contrario, cuando **Inicio de sesión** , se devuelve el valor de error MAPI_E_FAILONEPROVIDER desde su inicio de sesión, MAPI deshabilitar el servicio de mensajes a la que pertenece el proveedor. **Inicio de sesión** debe devolver MAPI_E_FAILONEPROVIDER si encuentra un error que no merece la pena la deshabilitación del servicio todo la vida de la sesión. Por ejemplo, un proveedor podría devolver este error cuando no permite la visualización de una interfaz de usuario y una contraseña requerida no está disponible. 
  
Si un proveedor devuelve MAPI_E_UNCONFIGURED desde su inicio de sesión, MAPI llamar a la función de entrada de servicio de mensajes del proveedor y, a continuación, vuelva a intentar el inicio de sesión. MAPI pasa MSG_SERVICE_CONFIGURE como el contexto para dar la oportunidad para que se configure el servicio. Si el cliente ha elegido permitir una interfaz de usuario en el inicio de sesión, el servicio puede presentar su hoja de propiedades de configuración, por lo que el usuario puede escribir información de configuración.
  
## <a name="see-also"></a>Vea también



[IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md)
  
[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)
  
[IMAPISession::OpenProfileSection](imapisession-openprofilesection.md)
  
[IMAPISupport::ModifyProfile](imapisupport-modifyprofile.md)
  
[IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)
  
[IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md)
  
[IProfSect : IMAPIProp](iprofsectimapiprop.md)
  
[MAPIERROR](mapierror.md)
  
[MSProviderInit](msproviderinit.md)
  
[IMSProvider : IUnknown](imsprovideriunknown.md)

