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

## <a name="parameters"></a>Parameters

 _lpMAPISup_
  
> a Un puntero al objeto actual de soporte MAPI para el almacén de mensajes.
    
 _ulUIParam_
  
> a Un controlador para la ventana primaria de los cuadros de diálogo o ventanas que este método muestra. 
    
 _lpszProfileName_
  
> a Un puntero a una cadena que contiene el nombre del perfil que se usa para el inicio de sesión del proveedor de almacenamiento. Esta cadena se puede mostrar en cuadros de diálogo, se escribe en un archivo de registro o simplemente se pasa por alto. Debe estar en formato Unicode si la marca MAPI_UNICODE se establece en el parámetro _ulFlags_ . 
    
 _cbEntryID_
  
> a Tamaño, en bytes, del identificador de entrada al que apunta el parámetro _lpEntryID_ . 
    
 _lpEntryID_
  
> a Un puntero al identificador de entrada para el almacén de mensajes. Pasar **null** en _lpEntryID_ indica que todavía no se ha seleccionado un almacén de mensajes y que se pueden presentar los cuadros de diálogo que permiten al usuario seleccionar un almacén de mensajes. 
    
 _ulFlags_
  
> a Una máscara de máscara de marcadores que controla cómo se realiza el inicio de sesión. Se pueden establecer los siguientes indicadores:
    
MAPI_DEFERRED_ERRORS 
  
> La llamada puede tener éxito incluso si el objeto subyacente no está disponible para la implementación que realiza la llamada. Si el objeto no está disponible, una llamada subsiguiente al objeto puede generar un error.
    
MAPI_UNICODE 
  
> Las cadenas pasadas están en formato Unicode. Si no se establece MAPI_UNICODE, las cadenas están en formato ANSI.
    
MDB_NO_DIALOG 
  
> Impide que se muestren los cuadros de diálogo de inicio de sesión. Si se establece esta marca, se devuelve el valor de error MAPI_E_LOGON_FAILED si el inicio de sesión no se ha realizado correctamente. Si no se establece esta marca, el proveedor de almacenamiento de mensajes puede pedir al usuario que corrija un nombre o una contraseña, que inserte un disco o que realice otras acciones necesarias para establecer una conexión con la tienda.
    
MDB_NO_MAIL 
  
> El almacén de mensajes no se debe usar para enviar o recibir correo. La marca indica MAPI que no debe notificar a la cola MAPI que se está abriendo este almacén de mensajes. Si se establece esta marca y el almacén de mensajes está estrechamente acoplado a un proveedor de transporte, el proveedor no necesita llamar al método [IMAPISupport:: SpoolerNotify](imapisupport-spoolernotify.md) . 
    
MDB_TEMPORARY 
  
> Registros en la tienda para que la información se pueda recuperar mediante programación desde la sección de perfil, sin usar cuadros de diálogo. Esta marca indica a MAPI que el almacén no se va a agregar a la tabla de almacén de mensajes y que el almacén no se puede convertir en permanente. Si se establece esta marca, los proveedores de almacenamiento de mensajes no tienen que llamar al método [IMAPISupport:: ModifyProfile](imapisupport-modifyprofile.md) . 
    
MDB_WRITE 
  
> Solicita el permiso de lectura y escritura.
    
 _lpInterface_
  
> a Un puntero al identificador de interfaz (IID) del almacén de mensajes en el que se va a iniciar sesión. Pasar **null** indica que se devuelve la interfaz MAPI para el almacén de mensajes ( [IMsgStore](imsgstoreimapiprop.md)). El parámetro _lpInterface_ también se puede establecer en un identificador para una interfaz adecuada para el almacén de mensajes (por ejemplo, IID_IUnknown o IID_IMAPIProp). 
    
 _lpcbSpoolSecurity_
  
> contempla Un puntero a la variable en la que el proveedor de almacén devuelve el tamaño, en bytes, de los datos de validación en el parámetro _lppbSpoolSecurity_ . 
    
 _lppbSpoolSecurity_
  
> contempla Un puntero al puntero a los datos de validación devueltos. Estos datos de validación se proporcionan para que el método [IMSProvider:: SpoolerLogon](imsprovider-spoolerlogon.md) pueda registrar la cola MAPI en el mismo almacén que el proveedor de almacenamiento de mensajes. 
    
 _lppMAPIError_
  
> contempla Un puntero a un puntero a la estructura [MAPIERROR](mapierror.md) devuelta, si existe, que contiene información de la versión, el componente y el contexto de un error. El parámetro _lppMAPIError_ puede establecerse en **null** si no hay ninguna estructura **MAPIERROR** para devolver. 
    
 _lppMSLogon_
  
> contempla Un puntero al puntero al objeto de inicio de sesión de un almacén de mensajes para que MAPI inicie sesión.
    
 _lppMDB_
  
> contempla Un puntero al puntero al objeto de almacén de mensajes para la cola MAPI y las aplicaciones cliente en las que se va a iniciar sesión.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
MAPI_E_FAILONEPROVIDER 
  
> Este proveedor no puede iniciar sesión, pero este error no debe deshabilitar el servicio. 
    
MAPI_E_LOGON_FAILED 
  
> No se pudo establecer una sesión de inicio de sesión.
    
MAPI_E_UNCONFIGURED 
  
> El perfil no contiene suficiente información para que el inicio de sesión se complete. Cuando se devuelve este valor, MAPI llama a la función de punto de entrada del servicio de mensajes del proveedor de almacenamiento de mensajes.
    
MAPI_E_USER_CANCEL 
  
> El usuario canceló la operación, normalmente haciendo clic en el botón **Cancelar** en un cuadro de diálogo. 
    
MAPI_E_UNKNOWN_CPID 
  
> El servidor no está configurado para admitir la página de códigos del cliente.
    
MAPI_E_UNKNOWN_LCID 
  
> El servidor no está configurado para admitir la información de la configuración regional del cliente.
    
MAPI_W_ERRORS_RETURNED 
  
> La llamada se realizó correctamente, pero el proveedor de almacenamiento de mensajes tiene información de error disponible. Cuando se devuelve esta advertencia, la llamada se debe administrar como correcta. Para probar esta advertencia, use la macro **HR_FAILED** . Para obtener más información, consulte [usar macros para el control de errores](using-macros-for-error-handling.md). Para obtener la información de error del proveedor, llame al método [IMAPISession:: GetLastError](imapisession-getlasterror.md) . 
    
## <a name="remarks"></a>Comentarios

MAPI llama al método **IMSProvider:: Logon** para realizar la mayor parte del procesamiento necesario para obtener acceso a un almacén de mensajes. Los proveedores de almacenamiento de mensajes validan las credenciales de usuario necesarias para tener acceso a un almacén en particular y devuelven un objeto de almacén de mensajes en el parámetro _lppMDB_ en el que la cola MAPI y las aplicaciones cliente pueden iniciar sesión. 
  
Además del objeto de almacén de mensajes devuelto para el uso de la cola MAPI y el cliente, el proveedor también devuelve un objeto de inicio de sesión del almacén de mensajes para que MAPI lo use en el control del almacén abierto. El objeto de inicio de sesión del almacén de mensajes y el objeto de almacén de mensajes deben estar estrechamente vinculados dentro del proveedor de almacén de mensajes para que cada uno pueda afectar al otro. El uso del objeto Store y del objeto de inicio de sesión debe ser idéntico; debe haber una correspondencia de uno a uno entre el objeto de inicio de sesión y el objeto de almacén de forma que los objetos actúen como si fueran un objeto que expone dos interfaces. Los dos objetos también deben crearse juntos y liberarse. 
  
El objeto compatible con MAPI, creado por MAPI y que se pasa al proveedor en el parámetro _lpMAPISup_ , proporciona acceso a las funciones de MAPI que requiere el proveedor. Entre ellas se incluyen funciones que guardan y recuperan información de perfil, acceso a libretas de direcciones, etc. El puntero _lpMAPISup_ puede ser diferente para cada almacén que se abre. Al procesar llamadas para un almacén de mensajes después del inicio de sesión, el proveedor del almacén debe usar la variable _lpMAPISup_ específica de ese almacén. Para cualquier llamada de **Inicio de sesión** que abra un almacén de mensajes y se realiza correctamente la creación de un objeto de inicio de sesión del almacén de mensajes, el proveedor debe guardar un puntero al objeto compatibilidad con MAPI en el objeto de inicio de sesión del almacén y debe llamar al método [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) para agregar una referencia para el objeto de compatibilidad. 
  
El parámetro _ulUIParam_ debe usarse si el proveedor presenta cuadros de diálogo durante la llamada de **Inicio de sesión** . Sin embargo, los cuadros de diálogo no se deben presentar si _ulFlags_ contiene la marca MDB_NO_DIALOG. Si es necesario llamar a una interfaz de usuario, pero _ulFlags_ no la permite, o bien, si por algún otro motivo no se puede mostrar la interfaz de usuario, el proveedor debe devolver MAPI_E_LOGON_FAILED. Si el **Inicio de sesión** muestra un cuadro de diálogo y el usuario cancela el inicio de sesión, normalmente haciendo clic en el botón **Cancelar** del cuadro de diálogo, el proveedor debe devolver MAPI_E_USER_CANCEL. 
  
El parámetro _lpEntryID_ puede ser **null** o apuntar a un identificador de entrada de almacén sin ajustar que este almacén de mensajes ha creado anteriormente. Si _lpEntryID_ apunta a un identificador de entrada no ajustado, el identificador de entrada puede provenir de uno de varios lugares: 
  
- Puede ser un identificador de entrada que el proveedor de almacenamiento ajustó previamente y escribió en la sección de perfil como **** una propiedad de un elemento ([PidTagEntryId](pidtagentryid-canonical-property.md)).
    
- Puede ser un identificador de entrada que el proveedor ajustó previamente y que se ha devuelto a un cliente de llamada como una propiedad **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)). 
    
- Puede ser un identificador de entrada que el proveedor ajustó previamente y que se ha devuelto a un cliente **** de llamada como la propiedad de un objeto de almacén de mensajes. 
    
En cualquiera de estos casos, es posible que el identificador de entrada se haya creado en un equipo distinto del que se usa actualmente.
  
Cuando _lpEntryID_ no es **null**, debe contener toda la información necesaria para identificar y localizar el almacén de mensajes. Esta información puede incluir nombres de volúmenes de red, números de teléfono, nombres de cuentas de usuario, etc. Si no se puede realizar la conexión al almacén con los datos del identificador de entrada, el proveedor de almacén debe mostrar un cuadro de diálogo que permita al usuario seleccionar la tienda que se va a abrir. Es posible que se requiera un cuadro de diálogo, por ejemplo, si se ha cambiado el nombre de un servidor, si se ha cambiado un nombre de cuenta o si no hay partes de la red disponibles.
  
Cuando _lpEntryID_ es **null**, no se ha seleccionado todavía el almacén de mensajes que se va a usar. El proveedor todavía puede tener acceso a un almacén sin mostrar un cuadro de diálogo si admite más métodos para especificar el almacén. Por ejemplo, el proveedor puede comprobar su archivo de inicialización o puede buscar propiedades adicionales que se han colocado en la sección de perfil del servicio de mensajes o en la configuración.
  
Si un proveedor encuentra que toda la información necesaria no está en el perfil, debe devolver MAPI_E_UNCONFIGURED. MAPI llamará a la función de punto de entrada del servicio de mensajes del proveedor para permitir que el usuario seleccione un almacén, o incluso para crear uno, y para que escriba un nombre de cuenta y una contraseña, según sea necesario. MAPI crea automáticamente una nueva sección de perfil para un nuevo almacén; Esta nueva sección de perfil puede ser temporal o permanente, en función de cómo se haya agregado. Si el proveedor de almacenamiento llama al método **IMAPISupport:: ModifyProfile** , la nueva sección de perfil se convierte en permanente y el almacén se agrega a la lista de los almacenes de mensajes devueltos por el método [IMAPISession:: GetMsgStoresTable](imapisession-getmsgstorestable.md) . 
  
El parámetro _lpInterface_ especifica el IID de la interfaz necesaria para el objeto Store recién abierto. Si se pasa **null** en _lpInterface_ , se especifica que se requiere la interfaz del almacén de mensajes MAPI **IMsgStore**. Al pasar el objeto de almacén de mensajes, IID_IMsgStore, también se especifica que se requiere **IMsgStore** . Si IID_IUnknown se pasa en _lpInterface_, el proveedor debe abrir el almacén utilizando la interfaz derivada de [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) es la mejor para el proveedor (de nuevo, suele ser **IMsgStore**). Cuando se pasa IID_IUnknown, la implementación de la llamada usa el método [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) para seleccionar una interfaz después de que la operación de apertura del almacén se haya realizado correctamente. 
  
La llamada de **IMSProvider:: Logon** debe devolver información suficiente, como una ruta de acceso al almacén y las credenciales para obtener acceso al almacén, para permitir que la cola de impresión MAPI inicie sesión en el mismo almacén que el proveedor del almacén sin presentar un cuadro de diálogo. Los parámetros _lpcbSpoolSecurity_ y _lppbSpoolSecurity_ se usan para devolver esta información. El proveedor asigna la memoria para estos datos pasando un puntero a un búfer en el parámetro _lpfAllocateBuffer_ de la función [MSProviderInit](msproviderinit.md) ; el proveedor coloca el tamaño de este búfer en _lpcbSpoolSecurity_. 
  
MAPI libera este búfer cuando corresponda. Si el inicio de sesión de la cola MAPI en el almacén solo se puede realizar a partir de la información de la sección de perfil, el proveedor puede devolver null en _lppbSpoolSecurity_ y 0 para el tamaño de la información en _lpcbSpoolSecurity_. El inicio de sesión de la cola MAPI se produce como parte de un proceso diferente que el inicio de sesión del almacén; como el búfer que contiene la información que se ha pasado se copia entre procesos, puede que no esté en la memoria en la misma ubicación que el proceso de cola MAPI que para el proceso del proveedor de almacén. Por lo tanto, un proveedor no debe poner direcciones en este búfer. Para obtener más información acerca del inicio de sesión de la cola MAPI, vea el método [IMSProvider:: SpoolerLogon](imsprovider-spoolerlogon.md) . 
  
La mayoría de los proveedores de almacenamiento usan el método [IMAPISession:: OpenProfileSection](imapisession-openprofilesection.md) del objeto de compatibilidad que se pasa en el parámetro _lpMAPISup_ para guardar y recuperar credenciales y opciones de usuario. **OpenProfileSection** permite a un proveedor de almacenamiento guardar información arbitraria adicional en una sección de perfil y asociarla con un recurso determinado. Por ejemplo, un proveedor de almacén puede guardar el nombre y la contraseña de la cuenta de usuario asociada a un recurso y cualquier ruta u otra información necesaria para tener acceso a ese recurso. 
  
Las propiedades con identificadores de propiedad 0x6600 a 0x67FF son propiedades seguras disponibles para el proveedor para su propio uso para almacenar datos privados en secciones de perfil. Para obtener más información sobre los usos de las propiedades de los objetos de sección de perfil, vea el método [IProfSect: IMAPIProp](iprofsectimapiprop.md) . 
  
Además de los datos privados de las propiedades con identificadores 0x6600 a través de 0x67FF, el proveedor de almacenamiento debe proporcionar información para la propiedad **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) en su sección de perfil. Debe ponerse en **PR_DISPLAY_NAME** el nombre para mostrar del proveedor en sí (una cadena de identificación, por ejemplo, "Microsoft Personal Information Store") que se muestra a los usuarios para que puedan distinguir este almacén de mensajes de otros que puedan tener acceso hasta. **PR_DISPLAY_NAME** suele contener un nombre de servidor, un nombre de cuenta de usuario o una ruta de acceso. 
  
Algunas propiedades de sección de perfil están visibles en la tabla de almacén de mensajes; otros son visibles durante la instalación, la instalación y la configuración del subsistema MAPI. Normalmente, el proveedor proporciona información para estas propiedades visibles para una nueva sección de perfil, que aún no incluye credenciales guardadas ni información privada, y cuando encuentra que la información de la propiedad ha cambiado. Para obtener más información acerca de las secciones de perfil, consulte [IMAPISupport:: OpenProfileSection](imapisupport-openprofilesection.md).
  
Después de iniciar sesión correctamente en un usuario y antes de volver a MAPI, el proveedor de almacenamiento debe crear la matriz de propiedades de la fila de estado para el recurso y llamar al método [IMAPISupport:: ModifyStatusRow](imapisupport-modifystatusrow.md) . 
  
 Las llamadas de **Inicio de sesión** que abren los almacenes de mensajes que ya están abiertos para la sesión MAPI actual omiten gran parte del procesamiento descrito anteriormente. Estas llamadas no crean filas de estado, devuelven objetos de inicio de sesión del almacén de mensajes, llaman a **AddRef** para el objeto compatible con MAPI o devuelven datos para el inicio de sesión de la cola MAPI. Estas llamadas devuelven S_OK y devuelven un objeto de almacén de mensajes con la interfaz solicitada. 
  
Para detectar estas llamadas, el proveedor debe mantener una lista en el objeto de proveedor de almacenamiento de mensajes de los almacenes que ya están abiertos para este objeto de proveedor. Al procesar una llamada de **Inicio de sesión** , el proveedor debe analizar esta lista de almacenes abiertos y determinar si el almacén en el que se va a iniciar sesión ya está abierto. Si es así, no es necesario comprobar las credenciales del usuario y, si es posible, se debe evitar mostrar un cuadro de diálogo. Si se deben mostrar los cuadros de diálogo, el proveedor debe comprobar la información devuelta para ver si un almacén se ha abierto una segunda vez. Además, el proveedor debe comprobar si hay aberturas duplicadas mediante _lpEntryID_ al principio del procesamiento de llamadas de **Inicio de sesión** . 
  
El procesamiento estándar para una llamada de **Inicio de sesión** que tiene acceso a un almacén abierto es el siguiente: 
  
1. El proveedor de almacén llama a **AddRef** para el objeto de almacén existente si la nueva interfaz que se solicita es la misma que la interfaz del almacén existente. De lo contrario, llama a **QueryInterface** para obtener la nueva interfaz. Si el almacén no admite la nueva interfaz, el proveedor devolverá el valor de error MAPI_E_INTERFACE_NOT_SUPPORTED. 
    
2. El proveedor devuelve un puntero a la interfaz necesaria del objeto Store existente en _lppMDB_.
    
3. El proveedor devuelve **null** en _lppMSLogon_.
    
4. El proveedor no debe abrir el perfil del objeto de soporte que se ha pasado en la llamada. Además, no debe registrar un identificador único de proveedor, registrar una fila de estado ni devolver los datos de inicio de sesión de la cola MAPI.
    
5. El proveedor no debe llamar a **AddRef** para el objeto support, porque no requiere un puntero al objeto. 
    
Siempre que sea posible, los proveedores deben devolver las cadenas de error y advertencia adecuadas para las llamadas de **Inicio de sesión** , ya que de este modo se facilita enormemente la carga de los usuarios a la hora de determinar por qué algo no funcionaba. Para devolver estas cadenas, un proveedor establece los miembros de la estructura **MAPIERROR** . MAPI busca, usa y libera la estructura **MAPIERROR** si la devuelve un proveedor. 
  
La memoria para esta estructura **MAPIERROR** debe asignarse mediante el búfer pasado en _lpfAllocateBuffer_ en la llamada **MSProviderInit** . Todas las cadenas de error contenidas en la estructura devuelta deben estar en formato Unicode si MAPI_UNICODE se establece en el ulFlags de **Inicio de sesión** _;_ en caso contrario, deben estar en el juego de caracteres ANSI. 
  
Para la mayoría de los valores de error devueltos desde el **Inicio de sesión**, MAPI deshabilita los servicios de mensajes a los que pertenece el proveedor que produce errores. MAPI no llamará a ningún proveedor que pertenezca a esos servicios durante la vida de la sesión MAPI. Por el contrario, cuando el **Inicio de sesión** devuelve el valor de error MAPI_E_FAILONEPROVIDER de su inicio de sesión, MAPI no deshabilita el servicio de mensajes al que pertenece el proveedor. El **Inicio de sesión** debe devolver MAPI_E_FAILONEPROVIDER si encuentra un error que no garantiza la deshabilitación de todo el servicio durante la vida de la sesión. Por ejemplo, un proveedor puede devolver este error cuando no permite mostrar una interfaz de usuario y una contraseña necesaria no está disponible. 
  
Si un proveedor devuelve MAPI_E_UNCONFIGURED desde su inicio de sesión, MAPI llamará a la función de entrada del servicio de mensajes del proveedor y, a continuación, volverá a intentar iniciar sesión. MAPI pasa MSG_SERVICE_CONFIGURE como contexto para dar al servicio una oportunidad de configurarse a sí mismo. Si el cliente ha elegido permitir una interfaz de usuario en el inicio de sesión, el servicio puede presentar su hoja de propiedades de configuración para que el usuario pueda escribir la información de configuración.
  
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

