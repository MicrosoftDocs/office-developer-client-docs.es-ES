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
ms.openlocfilehash: 9c7f62c69c7a06f7ca0e4bfddcf789cddc536ea6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309670"
---
# <a name="imsproviderlogon"></a>IMSProvider::Logon

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Registra MAPI en una instancia de un proveedor de almacenamiento de mensajes.
  
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
  
> [entrada] Puntero al objeto de soporte MAPI actual para el almacén de mensajes.
    
 _ulUIParam_
  
> [entrada] Identificador de la ventana principal de cualquier cuadro de diálogo o ventana que muestra este método. 
    
 _lpszProfileName_
  
> [entrada] Puntero a una cadena que contiene el nombre del perfil que se usa para el inicio de sesión del proveedor de almacenamiento. Esta cadena puede mostrarse en cuadros de diálogo, escribirse en un archivo de registro o simplemente omitirse. Debe estar en formato Unicode si la marca MAPI_UNICODE está establecida en el _parámetro ulFlags._ 
    
 _cbEntryID_
  
> [entrada] Tamaño, en bytes, del identificador de entrada al que apunta el _parámetro lpEntryID._ 
    
 _lpEntryID_
  
> [entrada] Puntero al identificador de entrada del almacén de mensajes. Pasar **null** en  _lpEntryID_ indica que aún no se ha seleccionado un almacén de mensajes y que se pueden presentar los cuadros de diálogo que permiten al usuario seleccionar un almacén de mensajes. 
    
 _ulFlags_
  
> [entrada] Máscara de bits de marcas que controla cómo se realiza el inicio de sesión. Se pueden establecer las siguientes marcas:
    
MAPI_DEFERRED_ERRORS 
  
> La llamada puede ser correcta incluso si el objeto subyacente no está disponible para la implementación de llamada. Si el objeto no está disponible, una llamada posterior al objeto podría generar un error.
    
MAPI_UNICODE 
  
> Las cadenas pasadas están en formato Unicode. Si MAPI_UNICODE no se establece, las cadenas están en formato ANSI.
    
MDB_NO_DIALOG 
  
> Impide que se muestren cuadros de diálogo de inicio de sesión. Si se establece esta marca, se devuelve el valor MAPI_E_LOGON_FAILED error si el inicio de sesión no se realiza correctamente. Si no se establece esta marca, el proveedor del almacén de mensajes puede pedir al usuario que corrija un nombre o contraseña, que inserte un disco o que realice otras acciones necesarias para establecer una conexión con el almacén.
    
MDB_NO_MAIL 
  
> El almacén de mensajes no debe usarse para enviar o recibir correo. La marca indica a MAPI que no debe notificar a la cola MAPI que se está abierto este almacén de mensajes. Si se establece esta marca y el almacén de mensajes está estrechamente asociado con un proveedor de transporte, el proveedor no necesita llamar al método [IMAPISupport::SpoolerNotify.](imapisupport-spoolernotify.md) 
    
MDB_TEMPORARY 
  
> Inicia sesión en el almacén para que la información se pueda recuperar mediante programación desde la sección de perfil, sin usar cuadros de diálogo. Esta marca indica a MAPI que el almacén no se debe agregar a la tabla del almacén de mensajes y que el almacén no se puede convertir en permanente. Si se establece esta marca, los proveedores de almacén de mensajes no necesitan llamar al [método IMAPISupport::ModifyProfile.](imapisupport-modifyprofile.md) 
    
MDB_WRITE 
  
> Solicita permiso de lectura y escritura.
    
 _lpInterface_
  
> [entrada] Puntero al identificador de interfaz (IID) en el que se debe iniciar sesión en el almacén de mensajes. Pasar **null** indica que se devuelve la interfaz MAPI para el almacén de mensajes ( [IMsgStore](imsgstoreimapiprop.md)). El  _parámetro lpInterface_ también se puede establecer en un identificador para una interfaz adecuada para el almacén de mensajes (por ejemplo, IID_IUnknown o IID_IMAPIProp). 
    
 _lpcbSpoolSecurity_
  
> [salida] Puntero a la variable en la que el proveedor de almacenamiento devuelve el tamaño, en bytes, de los datos de validación en el parámetro _lppbSpoolSecurity._ 
    
 _lppbSpoolSecurity_
  
> [salida] Puntero al puntero a los datos de validación devueltos. Estos datos de validación se proporcionan para que el método [IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md) pueda iniciar sesión en la cola MAPI en el mismo almacén que el proveedor del almacén de mensajes. 
    
 _lppMAPIError_
  
> [salida] Puntero a un puntero a la estructura [MAPIERROR](mapierror.md) devuelta, si existe, que contiene información de versión, componente y contexto de un error. El  _parámetro lppMAPIError_ se puede establecer en **null** si no hay ninguna **estructura MAPIERROR** que devolver. 
    
 _lppMSLogon_
  
> [salida] Puntero al puntero al objeto de inicio de sesión del almacén de mensajes para que MAPI inicie sesión.
    
 _lppMDB_
  
> [salida] Puntero al puntero al objeto de almacén de mensajes para que la cola MAPI y las aplicaciones cliente inicien sesión.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
MAPI_E_FAILONEPROVIDER 
  
> Este proveedor no puede iniciar sesión, pero este error no debe deshabilitar el servicio. 
    
MAPI_E_LOGON_FAILED 
  
> No se pudo establecer una sesión de inicio de sesión.
    
MAPI_E_UNCONFIGURED 
  
> El perfil no contiene información suficiente para que se complete el inicio de sesión. Cuando se devuelve este valor, MAPI llama a la función de punto de entrada del servicio de mensajes del proveedor del almacén de mensajes.
    
MAPI_E_USER_CANCEL 
  
> El usuario canceló la operación, normalmente haciendo clic en el **botón** Cancelar de un cuadro de diálogo. 
    
MAPI_E_UNKNOWN_CPID 
  
> El servidor no está configurado para admitir la página de códigos del cliente.
    
MAPI_E_UNKNOWN_LCID 
  
> El servidor no está configurado para admitir la información de configuración regional del cliente.
    
MAPI_W_ERRORS_RETURNED 
  
> La llamada se ha hecho correctamente, pero el proveedor del almacén de mensajes tiene información de error disponible. Cuando se devuelve esta advertencia, la llamada debe tratarse como correcta. Para probar esta advertencia, use la **macro HR_FAILED** datos. Para obtener más información, vea [Usar macros para el control de errores.](using-macros-for-error-handling.md) Para obtener la información de error del proveedor, llame al [método IMAPISession::GetLastError.](imapisession-getlasterror.md) 
    
## <a name="remarks"></a>Comentarios

MAPI llama al **método IMSProvider::Logon** para realizar la mayor parte del procesamiento necesario para obtener acceso a un almacén de mensajes. Los proveedores de almacenamiento de mensajes validan las credenciales de usuario necesarias para tener acceso a un almacén determinado y devolver un objeto de almacén de mensajes en el parámetro  _lppMDB_ en el que la cola MAPI y las aplicaciones cliente pueden iniciar sesión. 
  
Además del objeto de almacén de mensajes devuelto para el uso del cliente y la cola MAPI, el proveedor también devuelve un objeto de inicio de sesión del almacén de mensajes para que MAPI lo use en el control del almacén abierto. El objeto de inicio de sesión del almacén de mensajes y el objeto de almacén de mensajes deben estar estrechamente vinculados dentro del proveedor de al almacenamiento de mensajes para que cada uno pueda afectar al otro. El uso del objeto de almacén y el objeto de inicio de sesión debe ser idéntico; debe haber una correspondencia uno a uno entre el objeto de inicio de sesión y el objeto de almacén, de forma que los objetos actúen como si fuera un objeto que exponga dos interfaces. Los dos objetos también deben crearse juntos y liberarse juntos. 
  
El objeto de compatibilidad mapi, creado por MAPI y pasado al proveedor en el parámetro  _lpMAPISup,_ proporciona acceso a las funciones de MAPI que requiere el proveedor. Estas incluyen funciones que guarden y recuperen información de perfil, obtener acceso a libretas de direcciones, entre otras. El  _puntero lpMAPISup_ puede ser diferente para cada almacén que se abre. Durante el procesamiento de llamadas para un almacén de mensajes después del inicio de sesión, el proveedor del almacén debe usar la variable  _lpMAPISup_ que es específica de ese almacén. Para  cualquier llamada de inicio de sesión que abra un almacén de mensajes y cree correctamente un objeto de inicio de sesión del almacén de mensajes, el proveedor debe guardar un puntero al objeto de compatibilidad mapi en el objeto de inicio de sesión del almacén y debe llamar al método [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) para agregar una referencia al objeto de compatibilidad. 
  
El  _parámetro ulUIParam_ debe usarse si el proveedor presenta cuadros de diálogo durante la llamada **de inicio de** sesión. Sin embargo, no se deben presentar cuadros de diálogo  _si ulFlags_ contiene el MDB_NO_DIALOG marca. Si es necesario llamar a una interfaz de usuario pero  _ulFlags_ no la permite, o si por algún otro motivo no se puede mostrar una interfaz de usuario, el proveedor debe devolver MAPI_E_LOGON_FAILED. Si **inicio** de sesión muestra un cuadro de diálogo y el  usuario cancela el inicio de sesión, normalmente haciendo clic en el botón Cancelar del cuadro de diálogo, el proveedor debe devolver MAPI_E_USER_CANCEL. 
  
El  _parámetro lpEntryID_ puede ser **nulo** o apuntar a un identificador de entrada de almacén sin envolver que este almacén de mensajes creó anteriormente. Si  _lpEntryID_ apunta a un identificador de entrada sin envolver, dicho identificador de entrada puede provienen de uno de varios lugares: 
  
- Puede ser un identificador de entrada que el proveedor de almacenamiento envolvía previamente y escribió en la sección de perfil como una **propiedad PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).
    
- Puede ser un identificador de entrada que el proveedor ha ajustado previamente y devuelto a un cliente de llamada como una propiedad **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)). 
    
- Puede ser un identificador de entrada que el proveedor ha ajustado previamente y devuelto a un cliente de llamada como la propiedad **PR_ENTRYID** de un objeto de almacén de mensajes. 
    
En cualquiera de estos casos, es posible que el identificador de entrada se haya creado en un equipo distinto del que se está utilizando actualmente.
  
Cuando  _lpEntryID_ no es **nulo,** debe contener toda la información necesaria para identificar y localizar el almacén de mensajes. Esta información puede incluir nombres de volumen de red, números de teléfono, nombres de cuenta de usuario, entre otros. Si no se puede realizar la conexión al almacén mediante los datos del identificador de entrada, el proveedor del almacén debe mostrar un cuadro de diálogo que permita al usuario seleccionar el almacén que se va a abrir. Es posible que se necesite un cuadro de diálogo, por ejemplo, si se ha cambiado el nombre de un servidor, si se ha cambiado un nombre de cuenta o si partes de la red no están disponibles.
  
Cuando  _lpEntryID_ es **nulo,** el almacén de mensajes que se va a usar aún no se ha seleccionado. El proveedor aún puede tener acceso a un almacén sin mostrar un cuadro de diálogo si admite más métodos para especificar el almacén. Por ejemplo, el proveedor puede comprobar su archivo de inicialización o puede buscar propiedades adicionales que se colocaron en su sección de perfil del servicio de mensajes o en la sección de perfil de su servicio de mensajes en la configuración.
  
Si un proveedor encuentra que toda la información necesaria no está en el perfil, debe devolver MAPI_E_UNCONFIGURED. A continuación, MAPI llamará a la función de punto de entrada del servicio de mensajes del proveedor para permitir al usuario seleccionar un almacén, o incluso crear uno, y escribir un nombre de cuenta y una contraseña, según sea necesario. MAPI crea automáticamente una nueva sección de perfil para un nuevo almacén; esta nueva sección de perfil puede ser temporal o permanente, en función de cómo se haya agregado. Si el proveedor del almacén llama al método **IMAPISupport::ModifyProfile,** la nueva sección de perfil se convierte en permanente y el almacén se agrega a la lista de almacenes de mensajes devueltos por el método [IMAPISession::GetMsgStoresTable.](imapisession-getmsgstorestable.md) 
  
El  _parámetro lpInterface_ especifica el IID de la interfaz necesaria para el objeto de almacén recién abierto. Pasar **null** en  _lpInterface_ especifica que la interfaz de almacén de mensajes MAPI, **IMsgStore**, es necesaria. Pasar el objeto de almacén de mensajes, IID_IMsgStore, también especifica que se requiere **IMsgStore.** Si IID_IUnknown se pasa en  _lpInterface_, el proveedor debe abrir el almacén mediante cualquier interfaz derivada de [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) que sea mejor para el proveedor (de nuevo, suele ser **IMsgStore**). Cuando IID_IUnknown se pasa, la implementación de llamada usa el método [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) para seleccionar una interfaz después de que la operación de apertura del almacén se realiza correctamente. 
  
La llamada **IMSProvider::Logon** debe devolver información suficiente, como una ruta de acceso al almacén y credenciales para obtener acceso al almacén, para permitir que la cola MAPI inicie sesión en el mismo almacén que hace el proveedor del almacén sin presentar un cuadro de diálogo. Los  _parámetros lpcbSpoolSecurity_  _e lppbSpoolSecurity_ se usan para devolver esta información. El proveedor asigna la memoria para estos datos pasando un puntero a un búfer en el parámetro _lpfAllocateBuffer_ de la función [MSProviderInit;](msproviderinit.md) el proveedor coloca el tamaño de este búfer _en lpcbSpoolSecurity_. 
  
MAPI libera este búfer cuando corresponde. Si el inicio de sesión de la cola MAPI en el almacén se puede realizar solo a partir de la información de la sección de perfil, el proveedor puede devolver null en  _lppbSpoolSecurity_ y 0 para el tamaño de la información en  _lpcbSpoolSecurity_. El inicio de sesión de cola MAPI se produce como parte de un proceso diferente al inicio de sesión del almacén; dado que el búfer que contiene la información pasada se copia entre procesos, es posible que no esté en la memoria en la misma ubicación para el proceso de cola MAPI que para el proceso del proveedor de almacenamiento. Por lo tanto, un proveedor no debe colocar direcciones en este búfer. Para obtener más información acerca del inicio de sesión de la cola MAPI, vea el método [IMSProvider::SpoolerLogon.](imsprovider-spoolerlogon.md) 
  
La mayoría de los proveedores de almacén usan el método [IMAPISession::OpenProfileSection](imapisession-openprofilesection.md) del objeto de compatibilidad pasado en el parámetro  _lpMAPISup_ para guardar y recuperar credenciales y opciones de usuario. **OpenProfileSection permite** a un proveedor de almacén guardar información arbitraria adicional en una sección de perfil y asociarla a un recurso determinado. Por ejemplo, un proveedor de almacenamiento puede guardar el nombre de cuenta de usuario y la contraseña asociados a un recurso y cualquier ruta de acceso u otra información necesaria para tener acceso a ese recurso. 
  
Las propiedades con identificadores de 0x6600 a 0x67FF son propiedades seguras disponibles para el proveedor para su propio uso para almacenar datos privados en secciones de perfil. Para obtener más información acerca de los usos de propiedades en objetos de sección de perfil, vea el [método IProfSect : IMAPIProp](iprofsectimapiprop.md) . 
  
Además de los datos privados de las propiedades con identificadores 0x6600 a través de 0x67FF, el proveedor del almacén debe proporcionar información para la propiedad **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) en su sección de perfil. Debe incluir PR_DISPLAY_NAME el nombre para mostrar del proveedor en sí, una cadena de identificación (por ejemplo, "Almacén de información personal de Microsoft") que se muestra a los usuarios **para** que puedan distinguir este almacén de mensajes de otros a los que puedan tener acceso. **PR_DISPLAY_NAME** normalmente contiene un nombre de servidor, un nombre de cuenta de usuario o una ruta de acceso. 
  
Algunas propiedades de sección de perfil están visibles en la tabla del almacén de mensajes; otros son visibles durante la instalación, instalación y configuración del subsistema MAPI. Por lo general, el proveedor proporciona información para estas propiedades visibles para una nueva sección de perfil, que aún no incluye credenciales guardadas o información privada, y cuando encuentra que la información de la propiedad ha cambiado. Para obtener más información acerca de las secciones de perfil, [vea IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md).
  
Después de iniciar sesión correctamente en un usuario y antes de volver a MAPI, el proveedor del almacén debe crear la matriz de propiedades para la fila de estado del recurso y llamar al método [IMAPISupport::ModifyStatusRow.](imapisupport-modifystatusrow.md) 
  
 **Las** llamadas de inicio de sesión que abren los almacenes de mensajes que ya están abiertos para la sesión MAPI actual omiten gran parte del procesamiento descrito anteriormente. Estas llamadas no crean filas de estado, devuelven objetos de inicio de sesión del almacén de mensajes, llaman a **AddRef** para el objeto de compatibilidad mapi o devuelven datos para el inicio de sesión de cola MAPI. Estas llamadas devuelven S_OK y devuelven un objeto de almacén de mensajes con la interfaz solicitada. 
  
Para detectar estas llamadas, el proveedor debe mantener una lista en el objeto proveedor del almacén de mensajes de los almacenes que ya están abiertos para este objeto de proveedor. Al procesar una llamada **de** inicio de sesión, el proveedor debe examinar esta lista de almacenes abiertos y determinar si el almacén en el que se va a iniciar sesión ya está abierto. Si es así, no es necesario comprobar las credenciales de usuario y, si es posible, se debe evitar la visualización de un cuadro de diálogo. Si se deben mostrar cuadros de diálogo, el proveedor debe comprobar la información devuelta para ver si un almacén se ha abierto una segunda vez. Además, el proveedor debe comprobar si hay aperturas duplicadas mediante  _lpEntryID_ al principio del **procesamiento** de llamadas de inicio de sesión. 
  
El procesamiento estándar para una **llamada de** inicio de sesión que tiene acceso a un almacén abierto es el siguiente: 
  
1. El proveedor del almacén llama **a AddRef** para el objeto de almacén existente si la nueva interfaz que se solicita es la misma que la interfaz para el almacén existente. De lo contrario, llama **a QueryInterface** para obtener la nueva interfaz. Si el almacén no admite la nueva interfaz, el proveedor debe devolver el valor de error MAPI_E_INTERFACE_NOT_SUPPORTED. 
    
2. El proveedor devuelve un puntero a la interfaz necesaria del objeto de almacén existente  _en lppMDB_.
    
3. El proveedor devuelve **null** en  _lppMSLogon_.
    
4. El proveedor no debe abrir el perfil del objeto de soporte técnico pasado en la llamada. Además, no debe registrar un identificador único de proveedor, registrar una fila de estado ni devolver datos de inicio de sesión de cola MAPI.
    
5. El proveedor no debe llamar **a AddRef** para el objeto de compatibilidad, porque no requiere un puntero al objeto. 
    
Siempre que sea posible, los proveedores  deben devolver las cadenas de error y advertencia adecuadas para las llamadas de inicio de sesión, ya que al hacerlo se facilita enormemente la carga de los usuarios al determinar por qué algo no funcionaba. Para devolver estas cadenas, un proveedor establece los miembros de la **estructura MAPIERROR.** MAPI busca, usa y libera la estructura **MAPIERROR** si lo devuelve un proveedor. 
  
La memoria para **esta estructura MAPIERROR** debe asignarse mediante el búfer pasado _en lpfAllocateBuffer_ en la **llamada MSProviderInit.** Las cadenas de error contenidas en la estructura devuelta deben estar  en formato Unicode si MAPI_UNICODE se establece en el _ulFlags_ de inicio de sesión; de lo contrario, deben estar en el juego de caracteres ANSI. 
  
Para la mayoría de los valores de error devueltos desde **inicio** de sesión, MAPI deshabilita los servicios de mensajes a los que pertenece el proveedor con errores. MAPI no llamará a ningún proveedor que pertenezca a esos servicios durante el ciclo de vida de la sesión MAPI. Por el contrario, cuando **logon** devuelve el MAPI_E_FAILONEPROVIDER de error del inicio de sesión, MAPI no deshabilita el servicio de mensajes al que pertenece el proveedor. **El** inicio de sesión debe devolver MAPI_E_FAILONEPROVIDER si encuentra un error que no requiere deshabilitar todo el servicio durante la duración de la sesión. Por ejemplo, un proveedor puede devolver este error cuando no permite la visualización de una interfaz de usuario y una contraseña necesaria no está disponible. 
  
Si un proveedor devuelve MAPI_E_UNCONFIGURED de inicio de sesión, MAPI llamará a la función de entrada del servicio de mensajes del proveedor y, a continuación, volverá a intentar el inicio de sesión. MAPI pasa MSG_SERVICE_CONFIGURE como contexto para dar al servicio la oportunidad de configurarse a sí mismo. Si el cliente ha elegido permitir una interfaz de usuario durante el inicio de sesión, el servicio puede presentar su hoja de propiedades de configuración para que el usuario pueda escribir información de configuración.
  
## <a name="see-also"></a>Consulte también



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

