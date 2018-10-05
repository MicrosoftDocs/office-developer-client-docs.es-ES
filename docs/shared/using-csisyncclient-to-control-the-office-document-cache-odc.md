---
title: Uso de CSISyncClient para controlar la memoria caché de documentos de Office (ODC)
manager: soliver
ms.date: 07/13/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 394b8e6f-9132-4c98-8fd6-46ad3c871440
description: Obtenga información sobre cómo usar CSISyncClient para controlar la memoria caché de documentos de Office (ODC).
ms.openlocfilehash: ce33063f88492bcd6f9682a4a6431fb36f138d55
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399455"
---
# <a name="using-csisyncclient-to-control-the-office-document-cache-odc"></a>Uso de CSISyncClient para controlar la memoria caché de documentos de Office (ODC)

Obtenga información sobre cómo usar CSISyncClient para controlar la memoria caché de documentos de Office (ODC).
  
CSISyncClient es un servidor COM fuera de proceso (CsiSyncClient.exe) que permite que Microsoft OneDrive controlar el comportamiento de la memoria caché de documentos de Office (ODC). Por ejemplo, OneDrive puede recurrir a la ODC a través de CSISyncClient para cargar y descargar archivos a y desde los extremos habilitado MS-FSSHTTP. Esto habilita características avanzadas de seguridad de servicio en Office, como las transiciones de co-autoría y perfecta de sin conexión a en línea.
  
CsiSyncClient está disponible en el escritorio de Office (x86 y x64). Nota: Mientras que las versiones más recientes de Office es posible que se suministran con CsiSyncClient, el proceso se usará para la compatibilidad con versiones anteriores. La interfaz de CsiSyncClient y la metodología de controlar la ODC cambiará en futuras versiones de Office.
  
Actualmente se establece el identificador de clase para responder sólo a OneDrive.
  
El objeto COM es fácil de usar como servidor COM fuera de proceso y se ejecuta en CsiSyncClient.exe. Debido a las limitaciones con acceso (que utiliza la ODC), se distribuye con el tipo de bits que se incluye Office en x64 es así Office significa un x64 objeto COM o x86 Office significa un x86 objeto COM. Para evitar esta limitación, especificar CLSCTX_LOCAL_SERVER como parte de la CoCreateInstance tendrá el objeto COM se hospeda como un servidor de COM fuera de proceso, lo que permite la compatibilidad de bits cruzados.
  
## <a name="interfaces"></a>Interfaces

CSISyncClient usa las siguientes interfaces.
  
### <a name="interface-ilsclocalsyncclient"></a>Interfaz ILSCLocalSyncClient

Esto es la interfaz principal que se usa para sincronizar los archivos de Office.
  
- ProgID: Office.LocalSyncClient
- CLSID: {14286318-B6CF-49a1-81FC-D74AD94902F9}
- Biblioteca de tipos: {66CDD37F-D313-4e81-8C31-4198F3E42C3C}
   
Se utiliza el objeto COM que se expone como un servidor fuera de proceso. Especificar CLSCTX_LOCAL_SERVER como parte de CoCreateInstance permite la compatibilidad entre los procesos de 32 bits y 64 bits.
  
Una vez co-autoría que ha creado el objeto COM, se debe llamar a [ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) . Una vez [ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) haya finalizado correctamente, se puede llamar a cualquier API tantas veces como desee y en cualquier orden. También puede llamar a [ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) en un objeto ya inicializado, pero esto no tiene ningún efecto. 
  
Las excepciones al párrafo anterior son [ILSCLocalSyncClient::ResetCache](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) y [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize). Después de llamar a [ILSCLocalSyncClient::Uninitialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) en el objeto COM, debe destruir ese objeto y crear una nueva. [ILSCLocalSyncClient::ResetCache](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) eliminar su subcache, eliminar toda la información de archivo asociado en la memoria caché, pero dejar los documentos en el disco. También deja intacta para comunicarse con la memoria caché el estado. Esto le permite llamar a [ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) nuevo para crear una nueva memoria caché sin tener que destruir y volver a crear el objeto COM. 
  
**Funciones miembro públicas**

#### <a name="ilsclocalsyncclientdeletefile"></a>ILSCLocalSyncClient::DeleteFile

DeleteFile se usa para quitar la información del archivo de la memoria caché. Sin embargo, este método para dejar el archivo asociado en el disco y en el servidor.
  
`HRESULT ILSCLocalSyncClient::DeleteFile ([in] BSTR bstrResourceID)`

##### <a name="parameters"></a>Parámetros

 _bstrResourceID_
  
La cadena que identifica el ResourceID del archivo. Este valor debe ser no vacía con un máximo de 128 caracteres. 
  
##### <a name="return-values"></a>Valores devueltos

|Valor|Descripción|
|:-----|:-----|
|E_FAIL  <br/> |La llamada ha fallado.  <br/> |
|E_INVALIDARG  <br/> |Uno o más parámetros no son válidos.  <br/> |
|E_FAIL  <br/> |La llamada ha fallado.  <br/> |
|E_LSC_FILENOTFOUND  <br/> |El ResourceID determinado no está en la memoria caché.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |Initialize no se ha llamado correctamente en el pasado.  <br/> |
|E_LSC_PENDINGCHANGESINCACHE  <br/> |El archivo se está sincronizando o abrir y no se puede eliminar.  <br/> |
|S_OK  <br/> |La llamada ha sido correcta.  <br/> |
   
#### <a name="ilsclocalsyncclientgetchanges"></a>ILSCLocalSyncClient::GetChanges
<a name="ILSCLocalSyncClient_GetChanges"> </a>

GetChanges devuelve un enumerador de objetos de ILSCEvent y también devuelve un token que se asignó a la siguiente llamada para GetChanges, suponiendo que el consumidor ha procesado el conjunto de eventos anterior. Eventos antes de que el _nPreviousChangesToken_ especificado será eliminado y no está disponible. Si no hay ningún evento que va a procesar, _pnCurrentChangesToken_ debe ser el mismo valor que _nPreviousChangesToken_, pero aún se establecerá _ppiEvents_ . 
  
`HRESULT ILSCLocalSyncClient::GetChanges ([in] LONG nPreviousChangesToken, [out] LONG * pnCurrentChangesToken, [out] IEnumLSCEvent ** ppiEvents)`

##### <a name="parameters"></a>Parámetros

 _nPreviousChangesToken_
  
Identifica el evento que se procesó por última vez por el consumidor. 
  
 _pnCurrentChangesToken_
  
Identifica el evento más reciente que se pasa al consumidor. No debe ser null.
  
 _ppiEvents_
  
Enumerador para los eventos que se pasa al consumidor. No debe ser null. 
  
##### <a name="return-values"></a>Valores devueltos

|Valor|Descripción|
|:-----|:-----|
|E_FAIL  <br/> |La llamada ha fallado.  <br/> |
|E_INVALIDARG  <br/> |Uno o más parámetros no son válidos.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) no se ha llamado correctamente en el pasado.  <br/> |
|S_OK  <br/> |La llamada ha sido correcta.  <br/> |
   
#### <a name="ilsclocalsyncclientgetclientnetworksyncpermission"></a>ILSCLocalSyncClient::GetClientNetworkSyncPermission

GetClientNetworkSyncPermission se utiliza para consultar si heurística de sincronización de la oficina para el costo de red y se reemplaza el uso de la energía. Cuando en una 3G u otra red de alto costo, o cuando se ejecuta en batería frente a que se conecta, Office puede elegir esta opción Bloquear el tráfico de red hasta un momento más oportuno.
  
`HRESULT ILSCLocalSyncClient::GetClientNetworkSyncPermission ([in] LSCNetworkSyncPermissionType nspType, [out] VARIANT_BOOL * pfSyncEnabled)`

##### <a name="parameters"></a>Parámetros

 _nspType_
  
Marca que define qué heurística de costo a la consulta. Vea la [Enumeración LSCNetworkSyncPermissionType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType). 
  
 _pfSyncEnabled_
  
Especifica si la heurística de costo solicitado actualmente se reemplaza o no. No debe ser null. 
  
##### <a name="return-values"></a>Valores devueltos

|Valor|Descripción|
|:-----|:-----|
|E_FAIL  <br/> |La llamada ha fallado.  <br/> |
|E_INVALIDARG  <br/> |Uno o más parámetros no son válidos.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) no se ha llamado correctamente en el pasado.  <br/> |
|S_OK  <br/> |La llamada ha sido correcta.  <br/> |
   
#### <a name="ilsclocalsyncclientgetfilestatus"></a>ILSCLocalSyncClient::GetFileStatus

GetFileStatus se usa para recopilar información para un archivo específico: si existe en la memoria caché, si tiene pendientes de comunicación con la copia del servidor y, si tiene Office 2013 más hasta los datos de fecha de la copia local. Requiere un indicador de bit a bit de los valores de [Enumeración LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag) para determinar qué información es el objeto COM CsiSyncClient de consulta para. 
  
`HRESULT ILSCLocalSyncClient::GetFileStatus ([in] BSTR bstrResourceID, [in] LSCStatusFlag sfRequestedStatus, [out] BSTR * pbstrFileSystemPath, [out] BSTR * pbstrETag, [out] LSCStatusFlag * psfFileStatus)`

##### <a name="parameters"></a>Parámetros

 _bstrResourceID_
  
La cadena que identifica el archivo en el cliente. Este valor debe ser no vacías, con un máximo de 128 caracteres. 
  
 _sfRequestedStatus_
  
Marca que define la información que debe devolver. Vea la [Enumeración LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag). 
  
 _pbstrFileSystemPath_
  
La cadena que identifica la ubicación del archivo identificado por _bstrResourceID_ en el cliente. No debe ser null. 
  
 _pbstrETag_
  
Una cadena que va a contener el valor eTag para el archivo identificado por _bstrResourceID_. No debe ser null. 
  
 _psfFileStatus_
  
Marca que contendrá el estado solicitado a través de _sfRequestedStatus_ para el archivo identificado por _bstrResourceID_. No debe ser null. Vea la [Enumeración LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag). 
  
##### <a name="return-values"></a>Valores devueltos

|Valor|Descripción|
|:-----|:-----|
|E_FAIL  <br/> |La llamada ha fallado.  <br/> |
|E_INVALIDARG  <br/> |Uno o más parámetros no son válidos.  <br/> |
|E_LSC_FILENOTFOUND  <br/> |La información del archivo especificada por _bstrResourceID_ no existe en la memoria caché.  <br/> |
|E_LSC_LOCALFILEUNAVAILABLE  <br/> |Se ha solicitado LSCStatusFlag_LocalFileUnchanged o el archivo especificado por _bstrResourceID_ está bloqueado o que faltan.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) no se ha llamado correctamente en el pasado.  <br/> |
|S_OK  <br/> |La llamada ha sido correcta.  <br/> |
   
#### <a name="ilsclocalsyncclientgetsupportedfileextensions"></a>ILSCLocalSyncClient::GetSupportedFileExtensions
<a name="ILSCLocalSyncClient_GetSupportedFileExtensions"> </a>

GetSupportedFileExtensions devuelve una lista delimitada de extensiones de archivo que son compatibles actualmente con el objeto COM CsiSyncClient. Tenga en cuenta que esta lista puede cambiar, y el consumidor recibirá una notificación de un cambio a través del objeto IPartnerActivityCallback proporcionado en [ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) (vea EventOccured). 
  
Un ejemplo de la cadena devuelta es como sigue: "| docx | docm | pptx |"
  
`HRESULT ILSCLocalSyncClient::GetSupportedFileExtensions ([out] BSTR * pbstrSupportedFileExtensions)`

##### <a name="parameters"></a>Parámetros

 _pbstrSupportedFileExtensions_
  
Una cadena que se va a establecer con un conjunto delimitado por canalización de extensiones de archivo admitidas por el objeto COM CsiSyncClient. No debe ser null. 
  
##### <a name="return-values"></a>Valores devueltos

|Valor|Descripción|
|:-----|:-----|
|E_FAIL  <br/> |La llamada ha fallado.  <br/> |
|E_INVALIDARG  <br/> |Uno o más parámetros no son válidos.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) no se ha llamado correctamente en el pasado.  <br/> |
|S_OK  <br/> |La llamada ha sido correcta.  <br/> |
   
#### <a name="ilsclocalsyncclientinitialize"></a>ILSCLocalSyncClient::Initialize
<a name="ILSCLocalSyncClient_Initialize"> </a>

Initialize debe ser el primer método que se llama. De lo contrario, todas las otras API devolverá E_LSC_NOTINITIALIZED. Al llamar a Initialize en un objeto ya inicializado devuelve S_OK y no tiene ningún efecto. Si se devuelve E_LSC_CACHEMISMATCH, el llamador puede llamar a [ILSCLocalSyncClient::ResetCache](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) para eliminar la memoria caché asociada con el SuppliedID determinado. Sin embargo, en este caso otras API devolverá E_LSC_NOTINITIALIZED. 
  
`HRESULT ILSCLocalSyncClient::Initialize ([in] BSTR bstrSuppliedID, [in] BSTR bstrProgID, [in] BSTR bstrFileSystemDirectoryHint, [in] IPartnerActivityCallback * pEventCallback, [out] VARIANT_BOOL * pfCreatedNewCache)`

##### <a name="parameters"></a>Parámetros

 _bstrSuppliedID_
  
Identifica el consumidor y que la memoria caché para usar. Debe ser no vacía con un máximo de 32 caracteres. 
  
 _bstrProgID_
  
Identifica el objeto de COM del consumidor para la comunicación bidireccional. Debe ser no vacía con un máximo de 39 caracteres. Vea [ \<ProgID\> clave](https://docs.microsoft.com/windows/desktop/com/-progid--key) para obtener más información acerca de ProgIDs. 
  
 _bstrFileSystemDirectoryHint_
  
Identifica la raíz del directorio en el que se almacenarán los archivos locales. Debe ser no vacía con un máximo de 256 caracteres. El directorio ya debe existir. 
  
 _pEventCallback_
  
La interfaz de devolución de llamada que le notificará CsiSyncClient en los cambios. Vea IPartnerActivityCallback::EventOccurred. Este valor no debe ser null. 
  
 _pfCreatedNewCache_
  
Devuelve si se ha creado una nueva memoria caché. Si no hay memoria caché está asociada con la SuppliedID, se creará uno. Este valor no debe ser null.
  
##### <a name="return-values"></a>Valores devueltos

|Valor|Descripción|
|:-----|:-----|
|E_FAIL  <br/> |La llamada ha fallado.  <br/> |
|E_INVALIDARG  <br/> |Uno o más parámetros no son válidos.  <br/> |
|E_LSC_CACHEMISMATCH  <br/> |Un SuppliedID ya tiene una memoria caché asociada, pero tiene un ProgId o FileSystemDirectoryHint diferentes a los archivos proporcionados.  <br/> |
|E_LSC_DIRECTORYHINTCONFLICT  <br/> |El FileSystemDirectoryHint (o en una subcarpeta) ya existe en una caché diferente.  <br/> |
|E_LAC_PROGIDCONFLICT  <br/> |El ProgID ya existe en una caché diferente.  <br/> |
|S_OK  <br/> |La llamada ha sido correcta.  <br/> |
   
#### <a name="ilsclocalsyncclientlocalfilechange"></a>ILSCLocalSyncClient::LocalFileChange
<a name="ILSCLocalSyncClient_LocalFileChange"> </a>

LocalFileChange se usa para indicar el objeto COM CsiSyncClient para intentar cargar el archivo especificado. El método preparará el archivo para cargar, incluida la lectura del contenido del archivo actual. Si una carga ya está pendiente, se descartará la carga anterior y el nuevo contenido preparado para carga. Si el archivo está abierto para su edición en una aplicación, este método devuelve S_OK sin preparar el archivo de carga (debe hacer la aplicación ya este paso si hay cambios).
  
Este método le permitirá cargas si se marcó como carga bloqueados anteriormente (vea [ILSCLocalSyncClient::RenameFile ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile)).
  
`HRESULT ILSCLocalSyncClient::LocalFileChange ([in] BSTR bstrFileSystemPath, [in] BSTR bstrWebPath, [in] BSTR bstrResourceID)`

##### <a name="parameters"></a>Parámetros

 _bstrFileSystemPath_
  
Una cadena que identifica el archivo en el cliente. Este valor debe ser una ruta de acceso local no vacía con un máximo de 256 caracteres. Esta ruta de acceso debe estar en el árbol del directorio especificado por la FileSystemDirectoryHint cuando se realizó la llamada a [ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) . 
  
 _bstrResourceID_
  
Una cadena que identifica el ResourceID del archivo. Este valor debe ser no vacía con un máximo de 128 caracteres. 
  
 _bstrWebPath_
  
Una cadena que identifica el archivo en el servidor. Este valor debe ser la dirección URL no vacía, válido, pero no puede superar los INTERNET_MAX_URL_LENGTH, tal como se define por https://support.microsoft.com/kb/208427. 
  
##### <a name="return-values"></a>Valores devueltos

|Valor|Descripción|
|:-----|:-----|
|E_FAIL  <br/> |La llamada ha fallado.  <br/> |
|E_INVALIDARG  <br/> |Uno o más parámetros no son válidos.  <br/> |
|E_LSC_CONFLICTINGFILE  <br/> |El archivo especificado por _bstrFileSystemPath_ tiene un ResourceID diferente del especificado. Un evento de tipo LSCEventType_OnFilePathConflict se envía cuando se devuelve este error. Vea [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges).  <br/> |
|E_LSC_FILENOTFOUND  <br/> |El archivo fue eliminado operación intermedio.  <br/> |
|E_LSC_FILENOTSUPPORTED  <br/> |No se admite la extensión de archivo determinada por el objeto COM CsiSyncClient. Vea [ILSCLocalSyncClient::GetSupportedFileExtensions ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions).  <br/> |
|E_LSC_FILEUPTODATE  <br/> |El objeto COM no ha programado una carga debido a que el archivo en la memoria caché tenía los cambios más recientes desde el disco.  <br/> |
|E_LSC_LOCALFILEUNAVAILABLE  <br/> |El archivo especificado por _bstrFileSystemPath_ falta o está bloqueado.  <br/> |
|E_LSC_LOCALPATHNOTMAPPED  <br/> |El FileSystemPath determinado no está bajo la raíz del directorio especificada por la FileSystemDirectoryHint cuando se realizó la llamada a Initialize.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) no se ha llamado correctamente en el pasado.  <br/> |
|E_LSC_PATHMISMATCH  <br/> |El archivo especificado por _bstrResourceID_ tiene un FileSystemPath diferente del especificado.  <br/> |
|E_LSC_PENDINGCHANGESINCACHE  <br/> |El archivo especificado ya tiene cambios pendientes en una caché diferente y aún no se puede asociar con la memoria caché del consumidor.  <br/> |
|E_LSC_SERVERPATHINDIFFERENTCACHE  <br/> |El WebPath proporcionado entra en una caché diferente.  <br/> |
|S_OK  <br/> |La llamada ha sido correcta.  <br/> |
   
#### <a name="ilsclocalsyncclientrenamefile"></a>ILSCLocalSyncClient::RenameFile
<a name="ILSCLocalSyncClient_RenameFile"> </a>

RenameFile asocie una nueva dirección URL y la ruta de acceso local para un determinado ResourceID. Si el archivo especificado por el ResourceID ya no existe en la memoria caché, un intento de estarán para crearla y marcar para su descarga.
  
`HRESULT ILSCLocalSyncClient::RenameFile ([in] BSTR bstrResourceID, [in] BSTR bstrNewFileSystemPath, [in] BSTR bstrNewWebPath, [in] VARIANT_BOOL fBlockUploads)`

##### <a name="parameters"></a>Parámetros

 _bstrResourceID_
  
Una cadena que identifica el ResourceID del archivo. Este valor debe ser no vacía con un máximo de 128 caracteres. 
  
 _bstrNewFileSystemPath_
  
Una cadena que especifica la nueva ruta de acceso local para el archivo. Este valor debe ser una ruta de acceso local no vacía con un máximo de 256 caracteres. Esta ruta de acceso debe estar en el árbol del directorio especificado por la FileSystemDirectoryHint cuando se realizó la llamada a Initialize. 
  
 _bstrNewWebPath_
  
Una cadena que especifica la nueva dirección URL para el archivo. Este valor debe ser no vacías dirección URL válida, pero no puede superar los INTERNET_MAX_URL_LENGTH, tal como se define por https://support.microsoft.com/kb/208427. 
  
 _fBlockUploads_
  
Especifica si se permite la carga en la nueva ubicación actualmente. 
  
##### <a name="return-values"></a>Valores devueltos

|Valor|Descripción|
|:-----|:-----|
|E_FAIL  <br/> |La llamada ha fallado.  <br/> |
|E_INVALIDARG  <br/> |Uno o más parámetros no son válidos.  <br/> |
|E_LSC_CONFLICTINGFILE  <br/> |Las _bstrNewFileSystemPath_ o _bstrNewWebPath_ ya existen en otro archivo en cualquier caché. Un evento de tipo LSCEventType_OnFilePathConflict se envía cuando se devuelve este error. Vea [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges).  <br/> |
|E_LSC_FILENOTFOUND  <br/> |La información del archivo se ha eliminado de la memoria caché mientras se ejecuta este método.  <br/> |
|E_LSC_LOCALPATHNOTMAPPED  <br/> |El FileSystemPath determinado no está bajo la raíz del directorio especificada por la FileSystemDirectoryHint cuando se realizó la llamada a Initialize.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) no se ha llamado correctamente en el pasado.  <br/> |
|E_LSC_PENDINGCHANGESINCACHE  <br/> |El archivo especificado se está sincronizando en una aplicación de Office.  <br/> |
|S_OK  <br/> |La llamada ha sido correcta.  <br/> |
   
#### <a name="ilsclocalsyncclientresetcache"></a>ILSCLocalSyncClient::ResetCache
<a name="ILSCLocalSyncClient_ResetCache"> </a>

ResetCache, se eliminará de la memoria caché asociada con el SuppliedID que le ha proporcionado en Initialize. Esto incluye toda la información de archivo, pero dejará los archivos en el cliente y el servidor. Este método también deja el objeto en un estado parcialmente no inicializado. Las llamadas sólo es válidas después de esto son [ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) o [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize). Es posible que se llama a este método si Initialize se produce un error y devuelve E_LSC_CACHEMISMATCH y va a eliminar la memoria caché asociada con el SuppliedID que le ha proporcionado con la llamada con errores.
  
`HRESULT ILSCLocalSyncClient::ResetCache()`

##### <a name="parameters"></a>Parámetros

Ninguno
  
##### <a name="return-values"></a>Valores devueltos

|Valor|Descripción|
|:-----|:-----|
|E_FAIL  <br/> |La llamada ha fallado.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) no se ha llamado correctamente en el pasado.  <br/> |
|S_OK  <br/> |La llamada ha sido correcta.  <br/> |
   
#### <a name="ilsclocalsyncclientserverfilechange"></a>ILSCLocalSyncClient::ServerFileChange
<a name="ILSCLocalSyncClient_ServerFileChange"> </a>

ServerFileChange indica que el objeto COM CsiSyncClient para marcar el archivo especificado para su descarga. Si el archivo está abierto en una aplicación de Office para su edición, este método devuelve S_OK sin marcar el archivo para su descarga (la aplicación debe ya realice este paso si hay cambios).
  
Este método le permitirá descargas si se marcó como descargas bloqueados anteriormente (vea RenameFile).
  
`HRESULT ILSCLocalSyncClient::ServerFileChange ([in] BSTR bstrFileSystemPath, [in] BSTR bstrWebPath, [in] BSTR bstrResourceID)`

##### <a name="parameters"></a>Parámetros

|Parámetro|Descripción|
|:-----|:-----|
|bstrFileSystemPath  <br/> |Una cadena que identifica el archivo en el cliente. Este valor debe ser una ruta de acceso local no vacía con un máximo de 256 caracteres. Esta ruta de acceso debe estar en el árbol del directorio especificado por la FileSystemDirectoryHint cuando se realizó la llamada a Initialize.  <br/> |
|bstrResourceID  <br/> |Una cadena que identifica el ResourceID del archivo. Este valor debe ser no vacía con un máximo de 128 caracteres.  <br/> |
|bstrWebPath  <br/> |Una cadena que identifica el archivo en el servidor. Este valor debe ser una no vacías dirección URL válida, pero no puede superar los INTERNET_MAX_URL_LENGTH, tal como se define por https://support.microsoft.com/kb/208427.  <br/> |
   
##### <a name="return-values"></a>Valores devueltos

|Valor|Descripción|
|:-----|:-----|
|E_FAIL  <br/> |Error al establecer el estado de la conectividad de la memoria caché.  <br/> |
|E_LSC_CONFLICTINGFILE  <br/> |El archivo especificado por _bstrFileSystemPath_ tiene un ResourceID diferente del especificado.  <br/> |
|E_LSC_FILENOTSUPPORTED  <br/> |No se admite la extensión de archivo determinada por el objeto COM CsiSyncClient. Vea GetSupportedFileExtensions.  <br/> |
|E_LSC_FILENOTFOUND  <br/> |El archivo se ha eliminado en operación intermedio.  <br/> |
|E_INVALIDARG  <br/> |Uno o más parámetros no son válidos.  <br/> |
|E_LSC_LOCALPATHNOTMAPPED  <br/> |El FileSystemPath determinado no está bajo la raíz del directorio especificada por la FileSystemDirectoryHint cuando se realizó la llamada a Initialize.  <br/> |
|E_LSC_NOINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) no se ha llamado correctamente en el pasado.  <br/> |
|E_LSC_PATHMISMATCH  <br/> |El archivo especificado por _bstrResourceID_ tiene un FileSystemPath diferente del especificado.  <br/> |
|E_LSC_PENDINGCHANGESINCACHE  <br/> |El archivo especificado ya tiene cambios pendientes en una caché diferente y aún no se puede asociar con la memoria caché del consumidor.  <br/> |
|E_LSC_SERVERPATHINDIFFERENTCACHE  <br/> |El WebPath proporcionado entra en una caché diferente.  <br/> |
|S_OK  <br/> |La llamada ha sido correcta.  <br/> |
   
#### <a name="ilsclocalsyncclientsetclientconnectivitystate"></a>ILSCLocalSyncClient::SetClientConnectivityState
<a name="ILSCLocalSyncClient_ServerFileChange"> </a>

Establece la memoria caché en un estado en línea o sin conexión. Si están desconectados, Office no intenta comunicarse con el servidor para todos los archivos en esa memoria caché, independientemente de la configuración de _fBlockUploads_ de cada archivo individual. 
  
`HRESULT ILSCLocalSyncClient::SetClientConnectivityState ([in] VARIANT_BOOL fIsOnline)`

##### <a name="parameters"></a>Parámetros

 _fIsOnline_
  
Un valor booleano cómo determinar el estado de la conectividad de la memoria caché. 
  
##### <a name="return-values"></a>Valores devueltos

|Valor|Descripción|
|:-----|:-----|
|E_FAIL  <br/> |Error al establecer el estado de la conectividad de la memoria caché.  <br/> |
|E_INVALIDARG  <br/> |Uno o más parámetros no son válidos.  <br/> |
|E_LSC_NOINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) no se ha llamado correctamente en el pasado.  <br/> |
|S_OK  <br/> |La llamada ha sido correcta.  <br/> |
   
#### <a name="ilsclocalsyncclientsetclientnetworksyncpermission"></a>ILSCLocalSyncClient::SetClientNetworkSyncPermission
<a name="ILSCLocalSyncClient_ServerFileChange"> </a>

SetClientNetworkSyncPermission se usa para override o heurística de sincronización del restoreOffice para uso de costo y de la alimentación de la red. Cuando en una 3G u otra red de alto costo, o cuando se ejecuta en batería frente a que se conecta, Office puede elegir esta opción Bloquear el tráfico de red hasta un momento más oportuno. El consumidor de esta API puede usarla para reemplazar heurística de la oficina y forzar la sincronización para que se produzcan.
  
`HRESULT ILSCLocalSyncClient::SetClientNetworkSyncPermission ([in] LSCNetworkSyncPermissionType nspType, [in] VARIANT_BOOL fEnableSync)`

##### <a name="parameters"></a>Parámetros

 _nspType_
  
Marca que define qué heurística de costo para invalidar. Vea la [Enumeración LSCNetworkSyncPermissionType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType).
  
 _fEnableSync_
  
Especifica si para forzar la sincronización en, por lo tanto reemplazar esa heurística de costo, o ya no invalidarla. 
  
##### <a name="return-values"></a>Valores devueltos

|Valor|Descripción|
|:-----|:-----|
|E_FAIL  <br/> |Error al reemplazar heurística de sincronización.  <br/> |
|E_LSC_NOINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) no se ha llamado correctamente en el pasado.  <br/> |
|S_OK  <br/> |La llamada ha sido correcta.  <br/> |
   
#### <a name="ilsclocalsyncclientuninitialize"></a>ILSCLocalSyncClient::Uninitialize
<a name="ILSCLocalSyncClient_Uninitialize"> </a>

Descarga de la memoria caché desde el objeto COM y llevar a cabo operaciones de cierre. [ILSCLocalSyncClient::Uninitialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) DEBE llamarse antes de destruir el objeto COM. Después de llamar, no se puede llamar a ningún otras API, el objeto COM debe ser destruye y crea una nueva si desea continuar con las operaciones. 
  
`HRESULT ILSCLocalSyncClient::Uninitialize ()`

##### <a name="parameters"></a>Parámetros

Ninguno.
  
##### <a name="return-values"></a>Valores devueltos

|Valor|Descripción|
|:-----|:-----|
|E_FAIL  <br/> |Error al cancelar la inicialización.  <br/> |
|E_LSC_NOINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) no se ha llamado correctamente en el pasado.  <br/> |
|S_OK  <br/> |La llamada ha sido correcta.  <br/> |
   
### <a name="interface-ienumlscevent"></a>Interfaz IEnumLSCEvent

Esta interfaz representa una lista de eventos de ILSCEvent.
  
**Funciones miembro públicas**

#### <a name="ienumlsceventfnext"></a>IEnumLSCEvent::FNext

Recupera el siguiente evento de la lista de eventos.
  
`HRESULT IEnumLSCEvent::FNext ([out] ILSCEvent ** ppiLSCEvent)`

##### <a name="parameters"></a>Parámetros

 _ppiLSCEvent_
  
Un puntero a una interfaz ILSCEvent.
  
##### <a name="return-values"></a>Valores devueltos

|Valor|Descripción|
|:-----|:-----|
|E_FAIL  <br/> |No existen más eventos.  <br/> |
|S_OK  <br/> |La llamada tuvo éxito.  <br/> |
   
#### <a name="ienumlsceventreset"></a>IEnumLSCEvent::Reset

Restablece el enumerador al primer evento.
  
`HRESULT IEnumLSCEvent::Reset ()`

##### <a name="parameters"></a>Parámetros

Ninguno.
  
##### <a name="return-values"></a>Valores devueltos

Siempre devuelve S_OK. 
  
### <a name="interface-ilscevent"></a>Interfaz ILSCEvent

Esta interfaz representa un evento de sincronización. Toda la información sobre el evento se puede recuperar desde la interfaz.
  
**Funciones miembro públicas**

#### <a name="ilsceventgetconflictstatus"></a>ILSCEvent::GetConflictStatus

Tenga en cuenta que este valor se rellena cuando [ILSCLocalSyncClient::GetChanges](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) se llama, no cuando se creó el evento, por lo que sólo tendrá el estado actual del archivo, no el estado del archivo cuando cambia el estado de conflicto. 
  
Este valor sólo se llena cuando la [Enumeración LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) del evento es LSCEventType_OnLocalConflictStateChanged. 
  
`HRESULT ILSCEvent::GetConflictStatus ([out] VARIANT_BOOL * pfIsInConflict)`

##### <a name="parameters"></a>Parámetros

 _pfIsInConflict_
  
El estado actual de conflicto del archivo asociado con el evento.
  
##### <a name="return-values"></a>Valores devueltos

Siempre devuelve S_OK. 
  
#### <a name="ilsceventgeterror"></a>ILSCEvent::GetError

Este valor sólo se rellena cuando la [Enumeración LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) del evento es LSCEventType_OnServerChangesDownloaded o LSCEventType_OnLocalChangesUploaded. 
  
`HRESULT ILSCEvent::GetError ([out] LONG * pnError)`

##### <a name="parameters"></a>Parámetros

 _pnError_
  
El error asociado con este evento.
  
##### <a name="return-values"></a>Valores devueltos

Siempre devuelve S_OK. 
  
#### <a name="ilsceventgetetag"></a>ILSCEvent::GetETag

Este valor sólo se rellena cuando la [Enumeración LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) del evento es LSCEventType_OnServerChangesDownloaded o LSCEventType_OnLocalChangesUploaded. 
  
`HRESULT ILSCEvent::GetETag ([out] BSTR * pbstrETag)`

##### <a name="parameters"></a>Parámetros

 _pbstrETag_
  
El valor de ETag asociado a este evento
  
##### <a name="return-values"></a>Valores devueltos

Siempre devuelve S_OK. 
  
#### <a name="ilsceventgeteventtype"></a>ILSCEvent::GetEventType

Obtiene el tipo de este evento.
  
`HRESULT ILSCEvent::GetEventType ([out] LSCEventType * pnEventType)`

##### <a name="parameters"></a>Parámetros

 _pnEventType_
  
El tipo de evento de este evento. Vea [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) para los valores válidos. No debe ser null. 
  
##### <a name="return-values"></a>Valores devueltos

|Valor|Descripción|
|:-----|:-----|
|E_INVALIDARG  <br/> |Uno o más parámetros no son válidos.  <br/> |
|S_OK  <br/> |La llamada tuvo éxito.  <br/> |
   
#### <a name="ilsceventgetlocalworkingpath"></a>ILSCEvent::GetLocalWorkingPath

Obtiene la ruta de acceso local de trabajo para este evento.
  
`HRESULT ILSCEvent::GetLocalWorkingPath ([out] BSTR * pbstrLocalWorkingPath)`

##### <a name="parameters"></a>Parámetros

 _pbstrLocalWorkingPath_
  
La ruta de acceso local del archivo al que pertenece este evento. 
  
##### <a name="return-values"></a>Valores devueltos

Siempre devuelve S_OK. 
  
#### <a name="ilsceventgetresourceid"></a>ILSCEvent::GetResourceID

Obtiene el identificador de recurso para el evento.
  
`HRESULT ILSCEvent::GetResourceID ([out] BSTR * pbstrResourceID)`

##### <a name="parameters"></a>Parámetros

 _pbstrResourceID_
  
ResourceID del archivo asociado con este evento.
  
##### <a name="return-values"></a>Valores devueltos

Siempre devuelve S_OK. 
  
#### <a name="ilsceventgetresourceidattempted"></a>ILSCEvent::GetResourceIDAttempted

Este valor sólo se llena cuando la [Enumeración LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) del evento es LSCEventType_OnFilePathConflict. Cuando una llamada a [ILSCLocalSyncClient::LocalFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange), [ILSCLocalSyncClient::ServerFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange)o [ILSCLocalSyncClient::RenameFile](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) provocaría un conflicto de ruta de acceso Web o la ruta de acceso Local con otro archivo en la memoria caché de archivos de Office, esto se genera el evento. 
  
`HRESULT ILSCEvent::GetResourceIDAttempted ([out] BSTR * pbstrResourceIDAttempted)`

##### <a name="parameters"></a>Parámetros

 _pbstrResourceIDAttempted_
  
El ResourceID que causó este evento obtener generado. No debe ser null. 
  
##### <a name="return-values"></a>Valores devueltos

Siempre devuelve S_OK. 
  
#### <a name="ilsceventgetsyncerrortype"></a>ILSCEvent::GetSyncErrorType

Este valor sólo se rellena cuando la [Enumeración LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) del evento es LSCEventType_OnServerChangesDownloaded o LSCEventType_OnLocalChangesUploaded. 
  
`HRESULT ILSCEvent::GetSyncErrorType ([out] LSCEventSyncErrorType * pnSyncErrorType)`

##### <a name="parameters"></a>Parámetros

 _pnSyncErrorType_
  
El tipo de error asociado con este evento. Los valores posibles, vea [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) . No debe ser null. 
  
##### <a name="return-values"></a>Valores devueltos

|Valor|Descripción|
|:-----|:-----|
|E_INVALIDARG  <br/> |Uno o más parámetros no son válidos.  <br/> |
|S_OK  <br/> |La llamada tuvo éxito.  <br/> |
   
#### <a name="ilsceventgetwebpath"></a>ILSCEvent::GetWebPath

Este valor sólo se llena cuando la [Enumeración LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) del evento es LSCEventType_OnFilePathConflict. 
  
`HRESULT ILSCEvent::GetWebPath ([out] BSTR * pbstrWebPath)`

##### <a name="parameters"></a>Parámetros

 _pbstrWebPath_
  
Especifica la ruta de acceso Web asociado con este evento. No debe ser null. 
  
##### <a name="return-values"></a>Valores devueltos

Siempre devuelve S_OK. 
  
### <a name="interface-ilscevent2"></a>Interfaz ILSCEvent2

Esta interfaz contiene información adicional acerca de un evento de sincronización.
  
**Funciones miembro públicas**

#### <a name="ilscevent2geterrorchain"></a>ILSCEvent2::GetErrorChain

Obtiene la información de la cadena de error sobre un evento de sincronización.
  
`HRESULT ILSCEvent2::GetErrorChain ([out] BSTR * pbstrErrorChain)`

##### <a name="parameters"></a>Parámetros

 _pbstrErrorChain_
  
Una cadena que contenga la información de la cadena de error. No debe ser null. 
  
##### <a name="return-values"></a>Valores devueltos

|Valor|Descripción|
|:-----|:-----|
|E_NOTIMPL  <br/> |La versión instalada de Office no admite esta interfaz  <br/> |
|E_INVALIDARG  <br/> |Uno o varios de los valores de parámetro no son válidos.  <br/> |
|E_FAIL  <br/> |La información de la cadena de error no está disponible.  <br/> |
|S_OK  <br/> |La llamada tuvo éxito.  <br/> |
   
### <a name="interface-ipartneractivitycallback"></a>Interfaz IPartnerActivityCallback

Esta interfaz proporciona una función de devolución de llamada para el objeto COM CSISyncClient.
  
**Funciones miembro públicas**

#### <a name="ipartneractivitycallbackeventoccurred"></a>IPartnerActivityCallback::EventOccurred

Esto es una función de devolución de llamada en el objeto dado al objeto COM CsiSyncClient. Se espera que cuando se produce un evento (vea la [Enumeración LSCEventTypeOccurred](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred) para tipos de eventos válido), el objeto COM CsiSyncClient llamará a este método, el consumidor de señalización. 
  
`HRESULT IPartnerActivityCallback::EventOccurred ([in] LSCEventTypeOccurred eEventTypeOccurred)`

##### <a name="parameters"></a>Parámetros

 _eEventTypeOccurred_
  
El tipo de evento de este evento. Vea [Enum LSCEventTypeOccurred](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred) para los valores válidos. 
  
##### <a name="return-values"></a>Valores devueltos

Siempre devuelve S_OK.
  
## <a name="enumerations"></a>Enumeraciones

CSISyncClient usa las siguientes enumeraciones.
  
### <a name="enum-lsceventsyncerrortype"></a>Enumeración LSCEventSyncErrorType
<a name="Enum_LSCEventSyncErrorType"> </a>

Esta enumeración especifica las categorías de errores que pueden producirse durante la sincronización de un archivo.
  
|Enumerador|Descripción|
|:-----|:-----|
|LSCEventSyncErrorType_UserInterventionRequiredUnexpected  <br/> |El error de sincronización de este evento no se esperaba y es posible que requieren una consideración especial. De forma predeterminada, el usuario deba intervenir.  <br/> |
|LSCEventSyncErrorType_NoInterventionRequired  <br/> |El error de sincronización de este evento no necesitan una consideración especial. Office controla automáticamente.  <br/> |
|LSCEventSyncErrorType_UserInterventionRequired  <br/> |El error de sincronización de este evento requiere que un usuario resolverlo. Por ejemplo, error de conflicto de combinación requiere que un usuario abrir el documento y combinar.  <br/> |
|LSCEventSyncErrorType_WaitingOnClient  <br/> |El error de sincronización de este evento requiere el consumidor intervenir, pero no debe requieren una consideración especial por el usuario.  <br/> |
|LSCEventSyncErrorType_ClientInterventionRequired  <br/> |El error de sincronización de este evento requiere el consumidor a intervenir como un caso especial.  <br/> |
|LSCEventSyncErrorType_Max  <br/> ||
   
### <a name="enum-lsceventtype"></a>Enumeración LSCEventType
<a name="Enum_LSCEventType"> </a>

Esta enumeración especifica el tipo de eventos que se pueden producir por un archivo determinado.
  
|Enumerador|Descripción|
|:-----|:-----|
|LSCEventType_None  <br/> ||
|LSCEventType_OnLocalChanges  <br/> |Los cambios realizados en un archivo local.  <br/> |
|LSCEventType_OnOpenedByUser  <br/> |Un usuario abre un archivo.  <br/> |
|LSCEventType_OnServerChangesDownloaded  <br/> |Terminado de descargar los cambios del archivo desde el servidor.  <br/> |
|LSCEventType_OnLocalChangesUploaded  <br/> |Terminado de cargar los cambios de archivo en el servidor.  <br/> |
|LSCEventType_OnLocalConflictStateChanged  <br/> |El estado de conflicto de combinación de un archivo ha cambiado.  <br/> |
|LSCEventType_OnFileAdded  <br/> |Se ha agregado un archivo.  <br/> |
|LSCEventType_OnFileDeleted  <br/> |Se eliminó un archivo.  <br/> |
|LSCEventType_OnSyncEnabled  <br/> |Se habilitó la sincronización para los archivos de un usuario.  <br/> |
|LSCEventType_OnServerChangesDownloadStarted  <br/> |Comienza a descargar los cambios del archivo desde el servidor.  <br/> |
|LSCEventType_OnLocalChangesUploadStarted  <br/> |Cargar los cambios de archivo en el servidor se inició.  <br/> |
|LSCEventType_OnFilePathConflict  <br/> |Este evento se genera cuando una llamada a [ILSCLocalSyncClient::LocalFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange), [ILSCLocalSyncClient::ServerFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange), o [ILSCLocalSyncClient::RenameFile](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) hace que una ruta de acceso Web o la ruta de acceso Local colisión con otro archivo en el Memoria caché de archivos de Office.  <br/> |
|LSCEventType_OnFileForked  <br/> ||
|LSCEventType_Max  <br/> ||
   
### <a name="enum-lsceventtypeoccurred"></a>Enumeración LSCEventTypeOccurred
<a name="Enum_LSCEventTypeOccurred"> </a>

Esta enumeración especifica el tipo de eventos que se pueden producir. El consumidor debe llamar a funciones específicas de ILSCLocalSyncClient según el tipo de evento.
  
|Enumerador|Descripción|
|:-----|:-----|
|LSCEventTypeOccurred_GetChanges  <br/> |Se ha producido un ILSCEvent. El consumidor debe llamar a [ILSCLocalSyncClient::GetChanges](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) para recuperar los datos.  <br/> |
|LSCEventTypeOccurred_GetSupportedFileExtensions  <br/> |Han cambiado las extensiones de archivo compatibles. El consumidor debe llamar a [ILSCLocalSyncClient::GetSupportedFileExtensions](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions) para recuperar la nueva lista de extensiones admitidas.  <br/> |
   
### <a name="enum-lscnetworksyncpermissiontype"></a>Enumeración LSCNetworkSyncPermissionType
<a name="Enum_LSCNetworkSyncPermissionType"> </a>

Esta enumeración especifica los indicadores que se utilizan para una heurística de costo de la red. 

|Enumerador|Descripción|
|:-----|:-----|
|LSCNetworkSyncPermissionType_HighCost  <br/> |True si se invalida la heurística de costo para redes costosas (por ejemplo, 3 G).  <br/> |
|LSCNetworkSyncPermissionType_HighPowerUsage  <br/> |True si se invalida la heurística de costo para el uso de la energía (por ejemplo, una batería).  <br/> |
   
### <a name="enum-lscstatusflag"></a>Enumeración LSCStatusFlag
<a name="Enum_LSCStatusFlag"> </a>

Esta enumeración se usa para representar el estado de sincronización de un archivo. 
  
|Enumerador|Descripción|
|:-----|:-----|
|LCSStatusFlag_None  <br/> ||
|LSCStatusFlag_UploadPending  <br/> |Es True si no hay datos para enviar al archivo del servidor pendientes.  <br/> |
|LSCStatusFlag_DownloadPending  <br/> |Es True si no hay datos para descargar desde el archivo del servidor pendientes.  <br/> |
|LSCStatusFlag_LocalFileUnchanged  <br/> |Es True si los datos de Office tiene en el archivo en su memoria caché es la copia más reciente de los datos en el disco.  <br/> |
   

