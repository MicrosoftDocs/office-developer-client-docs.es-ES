---
title: Uso de CSISyncClient para controlar la Office de documentos (ODC)
manager: soliver
ms.date: 07/13/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 394b8e6f-9132-4c98-8fd6-46ad3c871440
description: Obtenga información sobre cómo usar CSISyncClient para controlar la Office de documentos (ODC).
ms.openlocfilehash: ce33063f88492bcd6f9682a4a6431fb36f138d55
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346259"
---
# <a name="using-csisyncclient-to-control-the-office-document-cache-odc"></a>Uso de CSISyncClient para controlar la Office de documentos (ODC)

Obtenga información sobre cómo usar CSISyncClient para controlar la Office de documentos (ODC).
  
CSISyncClient es un servidor COM fuera de proceso (CsiSyncClient.exe) que permite a Microsoft OneDrive controlar el comportamiento de la memoria caché de documentos (ODC) Office de documentos (ODC). Por ejemplo, OneDrive llamar a la ODC a través de CSISyncClient para cargar y descargar archivos desde y hacia los puntos de conexión habilitados para MS-FSSHTTP. Esto permite características avanzadas con respaldo de servicio en Office, como la co-autoría y transiciones perfectas de sin conexión a línea.
  
CsiSyncClient está disponible en Office Desktop (x86 y x64). Nota: Aunque las versiones más recientes de Office pueden enviarse con CsiSyncClient, el proceso se usará solo para compatibilidad con versiones anteriores. La interfaz CsiSyncClient y la metodología de control de ODC cambiarán en versiones futuras de Office.
  
El identificador de clase está establecido actualmente para responder solo a OneDrive.
  
El objeto COM es utilizable como un servidor COM fuera de proceso y se ejecuta en CsiSyncClient.exe. Debido a las limitaciones con Access (que usa la ODC), se incluye con el tipo de bits que Office incluye, por lo que x64 Office significa un objeto COM x64 o x86 Office significa un objeto COM x86. Para evitar esta limitación, al especificar CLSCTX_LOCAL_SERVER como parte de CoCreateInstance, el objeto COM se hospedará como un servidor COM fuera de proceso, lo que permitirá la compatibilidad entre bits.
  
## <a name="interfaces"></a>Interfaces

CSISyncClient usa las interfaces siguientes.
  
### <a name="interface-ilsclocalsyncclient"></a>Interfaz ILSCLocalSyncClient

Esta es la interfaz principal que se usa para sincronizar archivos en Office.
  
- ProgID: Office. LocalSyncClient
- CLSID: {14286318-B6CF-49a1-81FC-D74AD94902F9}
- TypeLib: {66CDD37F-D313-4e81-8C31-4198F3E42C3C}
   
El objeto COM que se expone se usa como un servidor fuera de proceso. La especificación CLSCTX_LOCAL_SERVER como parte de CoCreateInstance permite la compatibilidad entre procesos de 64 bits y 32 bits.
  
Una vez que haya co-creado el objeto COM, debe llamar primero a [ILSCLocalSyncClient::Initialize.](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) Una [vez que ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) se haya completado correctamente, puede llamar a cualquier API con la frecuencia que desee y en cualquier orden. También puede llamar a [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) en un objeto ya inicializado, pero esto no hace nada. 
  
Las excepciones al párrafo anterior son [ILSCLocalSyncClient::ResetCache ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) y [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize). Después de llamar [a ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) en el objeto COM, debe destruir ese objeto y crear uno nuevo. [ILSCLocalSyncClient::ResetCache ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) eliminará el subcaché, eliminará toda la información de archivo asociada en la memoria caché, pero dejará los documentos en el disco. También deja el estado intacto para comunicarse con la memoria caché. Esto le permite llamar a [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) de nuevo para crear una nueva memoria caché sin tener que destruir y volver a crear el objeto COM. 
  
**Funciones de miembro público**

#### <a name="ilsclocalsyncclientdeletefile"></a>ILSCLocalSyncClient::D eleteFile

DeleteFile se usa para quitar la información del archivo de la memoria caché. Sin embargo, este método dejará el archivo asociado en el disco y en el servidor.
  
`HRESULT ILSCLocalSyncClient::DeleteFile ([in] BSTR bstrResourceID)`

##### <a name="parameters"></a>Parameters

 _bstrResourceID_
  
Cadena que identifica el ResourceID del archivo. Este valor debe estar no vacío con un máximo de 128 caracteres. 
  
##### <a name="return-values"></a>Valores devueltos

|Valor|Descripción|
|:-----|:-----|
|E_FAIL  <br/> |La llamada ha fallado.  <br/> |
|E_INVALIDARG  <br/> |Uno o varios parámetros no son válidos.  <br/> |
|E_FAIL  <br/> |La llamada ha fallado.  <br/> |
|E_LSC_FILENOTFOUND  <br/> |El ResourceID especificado no está en la memoria caché.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |Initialize no se ha llamado correctamente en el pasado.  <br/> |
|E_LSC_PENDINGCHANGESINCACHE  <br/> |El archivo está sincronizado o abierto actualmente y no se puede eliminar.  <br/> |
|S_OK  <br/> |La llamada ha sido correcta.  <br/> |
   
#### <a name="ilsclocalsyncclientgetchanges"></a>ILSCLocalSyncClient::GetChanges
<a name="ILSCLocalSyncClient_GetChanges"> </a>

GetChanges devuelve un enumerador de objetos ILSCEvent y también devuelve un token que se proporciona a la siguiente llamada a GetChanges, suponiendo que el consumidor haya procesado el conjunto de eventos anterior. Los eventos anteriores  _al nPreviousChangesToken_ especificado se eliminarán y no estarán disponibles. Si no hay eventos que procesar,  _pnCurrentChangesToken_ debe ser el mismo valor que  _nPreviousChangesToken_, pero  _ppiEvents_ seguirá estando establecido. 
  
`HRESULT ILSCLocalSyncClient::GetChanges ([in] LONG nPreviousChangesToken, [out] LONG * pnCurrentChangesToken, [out] IEnumLSCEvent ** ppiEvents)`

##### <a name="parameters"></a>Parameters

 _nPreviousChangesToken_
  
Identifica qué evento se procesó por última vez por el consumidor. 
  
 _pnCurrentChangesToken_
  
Identifica el evento más reciente que se está entregando al consumidor. No debe ser null.
  
 _ppiEvents_
  
Un enumerador de los eventos entregados al consumidor. No debe ser null. 
  
##### <a name="return-values"></a>Valores devueltos

|Valor|Descripción|
|:-----|:-----|
|E_FAIL  <br/> |La llamada ha fallado.  <br/> |
|E_INVALIDARG  <br/> |Uno o varios parámetros no son válidos.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) no se ha llamado correctamente en el pasado.  <br/> |
|S_OK  <br/> |La llamada ha sido correcta.  <br/> |
   
#### <a name="ilsclocalsyncclientgetclientnetworksyncpermission"></a>ILSCLocalSyncClient::GetClientNetworkSyncPermission

GetClientNetworkSyncPermission se usa para consultar si se invalida la heurística de sincronización de Office para el costo de red y el uso de energía. Cuando se encuentra en una 3G u otra red de alto costo, o cuando se ejecuta con batería frente a estar conectado, Office puede optar por bloquear el tráfico de red hasta un momento más oportuno.
  
`HRESULT ILSCLocalSyncClient::GetClientNetworkSyncPermission ([in] LSCNetworkSyncPermissionType nspType, [out] VARIANT_BOOL * pfSyncEnabled)`

##### <a name="parameters"></a>Parameters

 _nspType_
  
Marca que define el costo heurístico de la consulta. Vea [Enum LSCNetworkSyncPermissionType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType). 
  
 _pfSyncEnabled_
  
Especifica si el costo heurístico solicitado está actualmente invalidado o no. No debe ser null. 
  
##### <a name="return-values"></a>Valores devueltos

|Valor|Descripción|
|:-----|:-----|
|E_FAIL  <br/> |La llamada ha fallado.  <br/> |
|E_INVALIDARG  <br/> |Uno o varios parámetros no son válidos.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) no se ha llamado correctamente en el pasado.  <br/> |
|S_OK  <br/> |La llamada ha sido correcta.  <br/> |
   
#### <a name="ilsclocalsyncclientgetfilestatus"></a>ILSCLocalSyncClient::GetFileStatus

GetFileStatus se usa para recopilar información para un archivo específico: si existe en la memoria caché, si tiene comunicación pendiente con la copia del servidor y si Office 2013 tiene los datos más actualizados de la copia local. Requiere una marca bit a bit de valores [Enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag) para determinar qué información debe consultar el objeto COM CsiSyncClient. 
  
`HRESULT ILSCLocalSyncClient::GetFileStatus ([in] BSTR bstrResourceID, [in] LSCStatusFlag sfRequestedStatus, [out] BSTR * pbstrFileSystemPath, [out] BSTR * pbstrETag, [out] LSCStatusFlag * psfFileStatus)`

##### <a name="parameters"></a>Parameters

 _bstrResourceID_
  
Cadena que identifica el archivo en el cliente. Este valor debe ser no vacío, con un máximo de 128 caracteres. 
  
 _sfRequestedStatus_
  
Una marca que define la información que se va a devolver. Vea [Enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag). 
  
 _pbstrFileSystemPath_
  
Cadena que identifica la ubicación del archivo identificado por  _bstrResourceID_ en el cliente. No debe ser null. 
  
 _pbstrETag_
  
Cadena que contendrá el eTag del archivo identificado por  _bstrResourceID_. No debe ser null. 
  
 _psfFileStatus_
  
Marca que contendrá el estado solicitado a través  _de sfRequestedStatus_ para el archivo identificado por  _bstrResourceID_. No debe ser null. Vea [Enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag). 
  
##### <a name="return-values"></a>Valores devueltos

|Valor|Descripción|
|:-----|:-----|
|E_FAIL  <br/> |La llamada ha fallado.  <br/> |
|E_INVALIDARG  <br/> |Uno o varios parámetros no son válidos.  <br/> |
|E_LSC_FILENOTFOUND  <br/> |La información de archivo especificada por  _bstrResourceID_ no existe en la memoria caché.  <br/> |
|E_LSC_LOCALFILEUNAVAILABLE  <br/> |LSCStatusFlag_LocalFileUnchanged se solicitó o el archivo especificado por  _bstrResourceID_ está bloqueado o falta.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) no se ha llamado correctamente en el pasado.  <br/> |
|S_OK  <br/> |La llamada ha sido correcta.  <br/> |
   
#### <a name="ilsclocalsyncclientgetsupportedfileextensions"></a>ILSCLocalSyncClient::GetSupportedFileExtensions
<a name="ILSCLocalSyncClient_GetSupportedFileExtensions"> </a>

GetSupportedFileExtensions devuelve una lista de extensiones de archivo delimitadas por canalización que son compatibles actualmente con el objeto COM CsiSyncClient. Tenga en cuenta que esta lista puede cambiar y se notificará al consumidor de un cambio a través del objeto IPartnerActivityCallback proporcionado en [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) (vea EventOccured). 
  
Un ejemplo de la cadena devuelta es el siguiente: "|docx|docm|pptx|"
  
`HRESULT ILSCLocalSyncClient::GetSupportedFileExtensions ([out] BSTR * pbstrSupportedFileExtensions)`

##### <a name="parameters"></a>Parameters

 _pbstrSupportedFileExtensions_
  
Cadena que se va a establecer con un conjunto delimitado por canalización de extensiones de archivo admitidas por el objeto COM CsiSyncClient. No debe ser null. 
  
##### <a name="return-values"></a>Valores devueltos

|Valor|Descripción|
|:-----|:-----|
|E_FAIL  <br/> |La llamada ha fallado.  <br/> |
|E_INVALIDARG  <br/> |Uno o varios parámetros no son válidos.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) no se ha llamado correctamente en el pasado.  <br/> |
|S_OK  <br/> |La llamada ha sido correcta.  <br/> |
   
#### <a name="ilsclocalsyncclientinitialize"></a>ILSCLocalSyncClient::Initialize
<a name="ILSCLocalSyncClient_Initialize"> </a>

Initialize debe ser el primer método llamado. De lo contrario, todas las demás API devolverán E_LSC_NOTINITIALIZED. Llamar a Initialize en un objeto ya inicializado devuelve S_OK y no hace nada. Si E_LSC_CACHEMISMATCH se devuelve, el autor de la llamada puede llamar a [ILSCLocalSyncClient::ResetCache ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) para eliminar la memoria caché asociada al SuppliedID dado. Sin embargo, en este caso, otras API seguirán E_LSC_NOTINITIALIZED. 
  
`HRESULT ILSCLocalSyncClient::Initialize ([in] BSTR bstrSuppliedID, [in] BSTR bstrProgID, [in] BSTR bstrFileSystemDirectoryHint, [in] IPartnerActivityCallback * pEventCallback, [out] VARIANT_BOOL * pfCreatedNewCache)`

##### <a name="parameters"></a>Parameters

 _bstrSuppliedID_
  
Identifica el consumidor y la memoria caché que se va a usar. Debe estar no vacío con un máximo de 32 caracteres. 
  
 _bstrProgID_
  
Identifica el objeto COM del consumidor para la comunicación bidireccional. Debe estar no vacío con un máximo de 39 caracteres. Consulte [ \< Clave ProgID \> ](https://docs.microsoft.com/windows/desktop/com/-progid--key) para obtener más información acerca de los ProgID. 
  
 _bstrFileSystemDirectoryHint_
  
Identifica la raíz del directorio en la que se almacenarán los archivos locales. Debe estar no vacío con un máximo de 256 caracteres. El directorio ya debe existir. 
  
 _pEventCallback_
  
La interfaz de devolución de llamada que CsiSyncClient notificará sobre los cambios. Consulta IPartnerActivityCallback::EventOccurred. Este valor no debe ser null. 
  
 _pfCreatedNewCache_
  
Devuelve si se creó una nueva memoria caché. Si no hay ninguna memoria caché asociada al SuppliedID, se creará una. Este valor no debe ser null.
  
##### <a name="return-values"></a>Valores devueltos

|Valor|Descripción|
|:-----|:-----|
|E_FAIL  <br/> |La llamada ha fallado.  <br/> |
|E_INVALIDARG  <br/> |Uno o varios parámetros no son válidos.  <br/> |
|E_LSC_CACHEMISMATCH  <br/> |Un SuppliedID ya tiene una memoria caché asociada, pero tiene un ProgId o FileSystemDirectoryHint diferente a los proporcionados.  <br/> |
|E_LSC_DIRECTORYHINTCONFLICT  <br/> |FileSystemDirectoryHint (o subcarpeta) ya existe en una memoria caché diferente.  <br/> |
|E_LAC_PROGIDCONFLICT  <br/> |El ProgID ya existe en una memoria caché diferente.  <br/> |
|S_OK  <br/> |La llamada ha sido correcta.  <br/> |
   
#### <a name="ilsclocalsyncclientlocalfilechange"></a>ILSCLocalSyncClient::LocalFileChange
<a name="ILSCLocalSyncClient_LocalFileChange"> </a>

LocalFileChange se usa para decir al objeto COM CsiSyncClient que intente cargar el archivo especificado. El método preparará el archivo para su carga, incluida la lectura del contenido actual del archivo. Si una carga ya está pendiente, se descartará la carga anterior y se preparará el nuevo contenido para la carga. Si el archivo está abierto para su edición en una aplicación, este método devolverá S_OK sin preparar el archivo para cargarlo (la aplicación ya debería realizar este paso si hay cambios).
  
Este método permitirá las cargas si se marcó como cargas bloqueadas anteriormente (vea [ILSCLocalSyncClient::RenameFile ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile)).
  
`HRESULT ILSCLocalSyncClient::LocalFileChange ([in] BSTR bstrFileSystemPath, [in] BSTR bstrWebPath, [in] BSTR bstrResourceID)`

##### <a name="parameters"></a>Parameters

 _bstrFileSystemPath_
  
Cadena que identifica el archivo en el cliente. Este valor debe ser una ruta de acceso local no vacía con un máximo de 256 caracteres. Esta ruta de acceso debe estar en el árbol de directorios especificado por FileSystemDirectoryHint cuando se realizó la llamada a [ILSCLocalSyncClient::Initialize.](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) 
  
 _bstrResourceID_
  
Cadena que identifica el ResourceID del archivo. Este valor debe estar no vacío con un máximo de 128 caracteres. 
  
 _bstrWebPath_
  
Cadena que identifica el archivo en el servidor. Este valor debe ser una dirección URL no vacía y válida, pero no más de INTERNET_MAX_URL_LENGTH, tal como se define en https://support.microsoft.com/kb/208427 . 
  
##### <a name="return-values"></a>Valores devueltos

|Valor|Descripción|
|:-----|:-----|
|E_FAIL  <br/> |La llamada ha fallado.  <br/> |
|E_INVALIDARG  <br/> |Uno o varios parámetros no son válidos.  <br/> |
|E_LSC_CONFLICTINGFILE  <br/> |El archivo especificado por  _bstrFileSystemPath_ tiene un ResourceID diferente del especificado. Se envía un evento de tipo LSCEventType_OnFilePathConflict cuando se devuelve este error. Vea [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges).  <br/> |
|E_LSC_FILENOTFOUND  <br/> |El archivo se eliminó en mitad de la operación.  <br/> |
|E_LSC_FILENOTSUPPORTED  <br/> |La extensión de archivo determinada no es compatible con el objeto COM CsiSyncClient. Vea [ILSCLocalSyncClient::GetSupportedFileExtensions ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions).  <br/> |
|E_LSC_FILEUPTODATE  <br/> |El objeto COM no programó una carga porque el archivo de la memoria caché tenía los cambios más recientes del disco.  <br/> |
|E_LSC_LOCALFILEUNAVAILABLE  <br/> |Falta o se bloquea el archivo especificado por _bstrFileSystemPath._  <br/> |
|E_LSC_LOCALPATHNOTMAPPED  <br/> |El FileSystemPath especificado no está en la raíz del directorio especificada por FileSystemDirectoryHint cuando se realizó la llamada a Initialize.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) no se ha llamado correctamente en el pasado.  <br/> |
|E_LSC_PATHMISMATCH  <br/> |El archivo especificado por  _bstrResourceID_ tiene un FileSystemPath diferente del especificado.  <br/> |
|E_LSC_PENDINGCHANGESINCACHE  <br/> |El archivo especificado ya tiene cambios pendientes en una memoria caché diferente y aún no se puede asociar a la memoria caché del consumidor.  <br/> |
|E_LSC_SERVERPATHINDIFFERENTCACHE  <br/> |El WebPath proporcionado se encuentra en una memoria caché diferente.  <br/> |
|S_OK  <br/> |La llamada ha sido correcta.  <br/> |
   
#### <a name="ilsclocalsyncclientrenamefile"></a>ILSCLocalSyncClient::RenameFile
<a name="ILSCLocalSyncClient_RenameFile"> </a>

RenameFile asociará una nueva dirección URL y una ruta de acceso local para un ResourceID determinado. Si el archivo especificado por ResourceID aún no existe en la memoria caché, se intentará crearlo y marcarlo para su descarga.
  
`HRESULT ILSCLocalSyncClient::RenameFile ([in] BSTR bstrResourceID, [in] BSTR bstrNewFileSystemPath, [in] BSTR bstrNewWebPath, [in] VARIANT_BOOL fBlockUploads)`

##### <a name="parameters"></a>Parameters

 _bstrResourceID_
  
Cadena que identifica el ResourceID del archivo. Este valor debe estar no vacío con un máximo de 128 caracteres. 
  
 _bstrNewFileSystemPath_
  
Cadena que especifica la nueva ruta de acceso local para el archivo. Este valor debe ser una ruta de acceso local no vacía con un máximo de 256 caracteres. Esta ruta de acceso debe estar en el árbol de directorios especificado por FileSystemDirectoryHint cuando se realizó la llamada a Initialize. 
  
 _bstrNewWebPath_
  
Cadena que especifica la nueva dirección URL del archivo. Este valor debe ser una dirección URL válida no vacía, pero no más de INTERNET_MAX_URL_LENGTH, tal como se define en https://support.microsoft.com/kb/208427 . 
  
 _fBlockUploads_
  
Especifica si las cargas a la nueva ubicación están permitidas actualmente. 
  
##### <a name="return-values"></a>Valores devueltos

|Valor|Descripción|
|:-----|:-----|
|E_FAIL  <br/> |La llamada ha fallado.  <br/> |
|E_INVALIDARG  <br/> |Uno o varios parámetros no son válidos.  <br/> |
|E_LSC_CONFLICTINGFILE  <br/> |_BstrNewFileSystemPath_ o _bstrNewWebPath_ ya existen en otro archivo en cualquier caché. Se envía un evento de tipo LSCEventType_OnFilePathConflict cuando se devuelve este error. Vea [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges).  <br/> |
|E_LSC_FILENOTFOUND  <br/> |La información del archivo se eliminó de la memoria caché mientras se ejecutaba este método.  <br/> |
|E_LSC_LOCALPATHNOTMAPPED  <br/> |El FileSystemPath especificado no está en la raíz del directorio especificada por FileSystemDirectoryHint cuando se realizó la llamada a Initialize.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) no se ha llamado correctamente en el pasado.  <br/> |
|E_LSC_PENDINGCHANGESINCACHE  <br/> |El archivo especificado se está sincronizando actualmente en una Office aplicación.  <br/> |
|S_OK  <br/> |La llamada ha sido correcta.  <br/> |
   
#### <a name="ilsclocalsyncclientresetcache"></a>ILSCLocalSyncClient::ResetCache
<a name="ILSCLocalSyncClient_ResetCache"> </a>

ResetCache eliminará la memoria caché asociada al SuppliedID que se proporcionó en Initialize. Esto incluye toda la información del archivo, pero dejará los archivos en el cliente y en el servidor. Este método también deja el objeto en un estado parcialmente no inicializado. Las únicas llamadas válidas después de esto son [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) o [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize). Se puede llamar a este método si se produce un error en Initialize y devuelve E_LSC_CACHEMISMATCH y se eliminará la memoria caché asociada con el SuppliedID que se proporcionó con la llamada con error.
  
`HRESULT ILSCLocalSyncClient::ResetCache()`

##### <a name="parameters"></a>Parámetros

Ninguno
  
##### <a name="return-values"></a>Valores devueltos

|Valor|Descripción|
|:-----|:-----|
|E_FAIL  <br/> |La llamada ha fallado.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) no se llamó correctamente en el pasado.  <br/> |
|S_OK  <br/> |La llamada ha sido correcta.  <br/> |
   
#### <a name="ilsclocalsyncclientserverfilechange"></a>ILSCLocalSyncClient::ServerFileChange
<a name="ILSCLocalSyncClient_ServerFileChange"> </a>

ServerFileChange indica al objeto COM CsiSyncClient que marque el archivo especificado para su descarga. Si el archivo está abierto en una aplicación de Office para su edición, este método devolverá S_OK sin marcar el archivo para su descarga (la aplicación ya debería realizar este paso si hay cambios).
  
Este método permitirá descargas si se marcó como descargas bloqueadas anteriormente (vea RenameFile).
  
`HRESULT ILSCLocalSyncClient::ServerFileChange ([in] BSTR bstrFileSystemPath, [in] BSTR bstrWebPath, [in] BSTR bstrResourceID)`

##### <a name="parameters"></a>Parámetros

|Parámetro|Descripción|
|:-----|:-----|
|bstrFileSystemPath  <br/> |Cadena que identifica el archivo en el cliente. Este valor debe ser una ruta de acceso local no vacía con un máximo de 256 caracteres. Esta ruta de acceso debe estar en el árbol de directorios especificado por FileSystemDirectoryHint cuando se realizó la llamada a Initialize.  <br/> |
|bstrResourceID  <br/> |Cadena que identifica el ResourceID del archivo. Este valor debe estar no vacío con un máximo de 128 caracteres.  <br/> |
|bstrWebPath  <br/> |Cadena que identifica el archivo en el servidor. Este valor debe ser una dirección URL válida no vacía, pero no más de INTERNET_MAX_URL_LENGTH, tal como se define en https://support.microsoft.com/kb/208427 .  <br/> |
   
##### <a name="return-values"></a>Valores devueltos

|Valor|Descripción|
|:-----|:-----|
|E_FAIL  <br/> |Error al establecer el estado de conectividad de la memoria caché.  <br/> |
|E_LSC_CONFLICTINGFILE  <br/> |El archivo especificado por  _bstrFileSystemPath_ tiene un ResourceID diferente del especificado.  <br/> |
|E_LSC_FILENOTSUPPORTED  <br/> |La extensión de archivo determinada no es compatible con el objeto COM CsiSyncClient. Consulte GetSupportedFileExtensions.  <br/> |
|E_LSC_FILENOTFOUND  <br/> |El archivo se eliminó en mitad de la operación.  <br/> |
|E_INVALIDARG  <br/> |Uno o varios parámetros no son válidos.  <br/> |
|E_LSC_LOCALPATHNOTMAPPED  <br/> |El FileSystemPath especificado no está en la raíz del directorio especificada por FileSystemDirectoryHint cuando se realizó la llamada a Initialize.  <br/> |
|E_LSC_NOINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) no se ha llamado correctamente en el pasado.  <br/> |
|E_LSC_PATHMISMATCH  <br/> |El archivo especificado por  _bstrResourceID_ tiene un FileSystemPath diferente del especificado.  <br/> |
|E_LSC_PENDINGCHANGESINCACHE  <br/> |El archivo especificado ya tiene cambios pendientes en una memoria caché diferente y aún no se puede asociar a la memoria caché del consumidor.  <br/> |
|E_LSC_SERVERPATHINDIFFERENTCACHE  <br/> |El WebPath proporcionado se encuentra en una memoria caché diferente.  <br/> |
|S_OK  <br/> |La llamada ha sido correcta.  <br/> |
   
#### <a name="ilsclocalsyncclientsetclientconnectivitystate"></a>ILSCLocalSyncClient::SetClientConnectivityState
<a name="ILSCLocalSyncClient_ServerFileChange"> </a>

Establece la memoria caché en un estado en línea o sin conexión. Si está sin conexión, Office intentará comunicarse con el servidor para los archivos de esa memoria caché, independientemente de la configuración _fBlockUploads_ de cada archivo individual. 
  
`HRESULT ILSCLocalSyncClient::SetClientConnectivityState ([in] VARIANT_BOOL fIsOnline)`

##### <a name="parameters"></a>Parameters

 _fIsOnline_
  
Boolean que determina el estado de conectividad de la memoria caché. 
  
##### <a name="return-values"></a>Valores devueltos

|Valor|Descripción|
|:-----|:-----|
|E_FAIL  <br/> |Error al establecer el estado de conectividad de la memoria caché.  <br/> |
|E_INVALIDARG  <br/> |Uno o varios parámetros no son válidos.  <br/> |
|E_LSC_NOINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) no se ha llamado correctamente en el pasado.  <br/> |
|S_OK  <br/> |La llamada ha sido correcta.  <br/> |
   
#### <a name="ilsclocalsyncclientsetclientnetworksyncpermission"></a>ILSCLocalSyncClient::SetClientNetworkSyncPermission
<a name="ILSCLocalSyncClient_ServerFileChange"> </a>

SetClientNetworkSyncPermission se usa para invalidar o restaurar la heurística de sincronización deOffice para el costo de red y el uso de energía. Cuando se encuentra en una 3G u otra red de alto costo, o cuando se ejecuta con batería frente a estar conectado, Office puede optar por bloquear el tráfico de red hasta un momento más oportuno. El consumidor de esta API puede usarlo para invalidar la heurística de Office y forzar la sincronización.
  
`HRESULT ILSCLocalSyncClient::SetClientNetworkSyncPermission ([in] LSCNetworkSyncPermissionType nspType, [in] VARIANT_BOOL fEnableSync)`

##### <a name="parameters"></a>Parameters

 _nspType_
  
Marca que define el costo heurístico que se va a invalidar. Vea [Enum LSCNetworkSyncPermissionType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType).
  
 _fEnableSync_
  
Especifica si se debe forzar la sincronización, por lo que se invalida ese costo heurístico o si se deja de invalidar. 
  
##### <a name="return-values"></a>Valores devueltos

|Valor|Descripción|
|:-----|:-----|
|E_FAIL  <br/> |Error al invalidar la heurística de sincronización.  <br/> |
|E_LSC_NOINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) no se ha llamado correctamente en el pasado.  <br/> |
|S_OK  <br/> |La llamada ha sido correcta.  <br/> |
   
#### <a name="ilsclocalsyncclientuninitialize"></a>ILSCLocalSyncClient::Uninitialize
<a name="ILSCLocalSyncClient_Uninitialize"> </a>

Descarga la memoria caché del objeto COM y realiza operaciones de cierre. [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) DEBE llamarse antes de destruir el objeto COM. Una vez que se llama, no se puede llamar a otras API, se debe destruir el objeto COM y crear una nueva si desea continuar las operaciones. 
  
`HRESULT ILSCLocalSyncClient::Uninitialize ()`

##### <a name="parameters"></a>Parámetros

Ninguno.
  
##### <a name="return-values"></a>Valores devueltos

|Valor|Descripción|
|:-----|:-----|
|E_FAIL  <br/> |Error al cancelar la inicialización.  <br/> |
|E_LSC_NOINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) no se ha llamado correctamente en el pasado.  <br/> |
|S_OK  <br/> |La llamada ha sido correcta.  <br/> |
   
### <a name="interface-ienumlscevent"></a>Interfaz IEnumLSCEvent

Esta interfaz representa una lista de eventos ILSCEvent.
  
**Funciones de miembro público**

#### <a name="ienumlsceventfnext"></a>IEnumLSCEvent::FNext

Recupera el siguiente evento de la lista de eventos.
  
`HRESULT IEnumLSCEvent::FNext ([out] ILSCEvent ** ppiLSCEvent)`

##### <a name="parameters"></a>Parameters

 _ppiLSCEvent_
  
Puntero a una interfaz ILSCEvent.
  
##### <a name="return-values"></a>Valores devueltos

|Valor|Descripción|
|:-----|:-----|
|E_FAIL  <br/> |No hay más eventos.  <br/> |
|S_OK  <br/> |La llamada se ha realizado correctamente.  <br/> |
   
#### <a name="ienumlsceventreset"></a>IEnumLSCEvent::Reset

Restablece el enumerador al primer evento.
  
`HRESULT IEnumLSCEvent::Reset ()`

##### <a name="parameters"></a>Parámetros

Ninguno.
  
##### <a name="return-values"></a>Valores devueltos

Siempre devuelve S_OK. 
  
### <a name="interface-ilscevent"></a>Interfaz ILSCEvent

Esta interfaz representa un evento de sincronización. Toda la información sobre el evento se puede recuperar desde la interfaz.
  
**Funciones de miembro público**

#### <a name="ilsceventgetconflictstatus"></a>ILSCEvent::GetConflictStatus

Tenga en cuenta que este valor se rellena cuando se llama a [ILSCLocalSyncClient::GetChanges, ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) no cuando se creó el evento, por lo que solo tendrá el estado actual del archivo, no el estado del archivo cuando cambió el estado de conflicto. 
  
Este valor solo se rellena cuando [el enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) del evento se LSCEventType_OnLocalConflictStateChanged. 
  
`HRESULT ILSCEvent::GetConflictStatus ([out] VARIANT_BOOL * pfIsInConflict)`

##### <a name="parameters"></a>Parameters

 _pfIsInConflict_
  
El estado de conflicto actual del archivo asociado al evento.
  
##### <a name="return-values"></a>Valores devueltos

Siempre devuelve S_OK. 
  
#### <a name="ilsceventgeterror"></a>ILSCEvent::GetError

Este valor solo se rellena cuando [el enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) del evento se LSCEventType_OnServerChangesDownloaded o LSCEventType_OnLocalChangesUploaded. 
  
`HRESULT ILSCEvent::GetError ([out] LONG * pnError)`

##### <a name="parameters"></a>Parameters

 _pnError_
  
Error asociado a este evento.
  
##### <a name="return-values"></a>Valores devueltos

Siempre devuelve S_OK. 
  
#### <a name="ilsceventgetetag"></a>ILSCEvent::GetETag

Este valor solo se rellena cuando [el enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) del evento se LSCEventType_OnServerChangesDownloaded o LSCEventType_OnLocalChangesUploaded. 
  
`HRESULT ILSCEvent::GetETag ([out] BSTR * pbstrETag)`

##### <a name="parameters"></a>Parameters

 _pbstrETag_
  
ETag asociado a este evento
  
##### <a name="return-values"></a>Valores devueltos

Siempre devuelve S_OK. 
  
#### <a name="ilsceventgeteventtype"></a>ILSCEvent::GetEventType

Obtiene el tipo de este evento.
  
`HRESULT ILSCEvent::GetEventType ([out] LSCEventType * pnEventType)`

##### <a name="parameters"></a>Parameters

 _pnEventType_
  
Tipo de evento de este evento. Consulte [Enum LSCEventType para](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) obtener valores válidos. No debe ser null. 
  
##### <a name="return-values"></a>Valores devueltos

|Valor|Descripción|
|:-----|:-----|
|E_INVALIDARG  <br/> |Uno o varios parámetros no son válidos.  <br/> |
|S_OK  <br/> |La llamada se ha realizado correctamente.  <br/> |
   
#### <a name="ilsceventgetlocalworkingpath"></a>ILSCEvent::GetLocalWorkingPath

Obtiene la ruta de acceso de trabajo local para este evento.
  
`HRESULT ILSCEvent::GetLocalWorkingPath ([out] BSTR * pbstrLocalWorkingPath)`

##### <a name="parameters"></a>Parameters

 _pbstrLocalWorkingPath_
  
La ruta de acceso local del archivo al que pertenece este evento. 
  
##### <a name="return-values"></a>Valores devueltos

Siempre devuelve S_OK. 
  
#### <a name="ilsceventgetresourceid"></a>ILSCEvent::GetResourceID

Obtiene el identificador de recurso del evento.
  
`HRESULT ILSCEvent::GetResourceID ([out] BSTR * pbstrResourceID)`

##### <a name="parameters"></a>Parameters

 _pbstrResourceID_
  
ResourceID del archivo asociado a este evento.
  
##### <a name="return-values"></a>Valores devueltos

Siempre devuelve S_OK. 
  
#### <a name="ilsceventgetresourceidattempted"></a>ILSCEvent::GetResourceIDAttempted

Este valor solo se rellena cuando [el enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) del evento se LSCEventType_OnFilePathConflict. Cuando una llamada a [ILSCLocalSyncClient::LocalFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange), [ILSCLocalSyncClient::ServerFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange)o [ILSCLocalSyncClient::RenameFile](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) provocaría una colisión de ruta de acceso web o ruta de acceso local con otro archivo en la memoria caché de archivos de Office, se genera este evento. 
  
`HRESULT ILSCEvent::GetResourceIDAttempted ([out] BSTR * pbstrResourceIDAttempted)`

##### <a name="parameters"></a>Parameters

 _pbstrResourceIDAttempted_
  
ResourceID que provocó que se generara este evento. No debe ser null. 
  
##### <a name="return-values"></a>Valores devueltos

Siempre devuelve S_OK. 
  
#### <a name="ilsceventgetsyncerrortype"></a>ILSCEvent::GetSyncErrorType

Este valor solo se rellena cuando [el enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) del evento se LSCEventType_OnServerChangesDownloaded o LSCEventType_OnLocalChangesUploaded. 
  
`HRESULT ILSCEvent::GetSyncErrorType ([out] LSCEventSyncErrorType * pnSyncErrorType)`

##### <a name="parameters"></a>Parameters

 _pnSyncErrorType_
  
Tipo de error asociado a este evento. Vea [Enum LSCEventType para](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) ver los valores potenciales. No debe ser null. 
  
##### <a name="return-values"></a>Valores devueltos

|Valor|Descripción|
|:-----|:-----|
|E_INVALIDARG  <br/> |Uno o varios parámetros no son válidos.  <br/> |
|S_OK  <br/> |La llamada se ha realizado correctamente.  <br/> |
   
#### <a name="ilsceventgetwebpath"></a>ILSCEvent::GetWebPath

Este valor solo se rellena cuando [el enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) del evento se LSCEventType_OnFilePathConflict. 
  
`HRESULT ILSCEvent::GetWebPath ([out] BSTR * pbstrWebPath)`

##### <a name="parameters"></a>Parameters

 _pbstrWebPath_
  
Especifica la ruta de acceso web asociada a este evento. No debe ser null. 
  
##### <a name="return-values"></a>Valores devueltos

Siempre devuelve S_OK. 
  
### <a name="interface-ilscevent2"></a>Interfaz ILSCEvent2

Esta interfaz contiene información adicional sobre un evento de sincronización.
  
**Funciones de miembro público**

#### <a name="ilscevent2geterrorchain"></a>ILSCEvent2::GetErrorChain

Obtiene la información de la cadena de errores sobre un evento de sincronización.
  
`HRESULT ILSCEvent2::GetErrorChain ([out] BSTR * pbstrErrorChain)`

##### <a name="parameters"></a>Parameters

 _pbstrErrorChain_
  
Cadena para contener la información de la cadena de errores. No debe ser null. 
  
##### <a name="return-values"></a>Valores devueltos

|Valor|Descripción|
|:-----|:-----|
|E_NOTIMPL  <br/> |La versión instalada de Office no admite esta interfaz  <br/> |
|E_INVALIDARG  <br/> |Uno o varios de los valores de parámetro no son válidos.  <br/> |
|E_FAIL  <br/> |La información de la cadena de errores no está disponible.  <br/> |
|S_OK  <br/> |La llamada se ha realizado correctamente.  <br/> |
   
### <a name="interface-ipartneractivitycallback"></a>Interfaz IPartnerActivityCallback

Esta interfaz proporciona una función de devolución de llamada al objeto COM CSISyncClient.
  
**Funciones de miembro público**

#### <a name="ipartneractivitycallbackeventoccurred"></a>IPartnerActivityCallback::EventOccurred

Se trata de una función de devolución de llamada en el objeto dado al objeto COM CsiSyncClient. Se espera que cuando se produzca un evento (vea [Enum LSCEventTypeOccurred](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred) para tipos de eventos válidos), el objeto COM CsiSyncClient llamará a este método y señalizará al consumidor. 
  
`HRESULT IPartnerActivityCallback::EventOccurred ([in] LSCEventTypeOccurred eEventTypeOccurred)`

##### <a name="parameters"></a>Parameters

 _eEventTypeOccurred_
  
Tipo de evento de este evento. Consulte [Enum LSCEventTypeOccurred para](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred) obtener valores válidos. 
  
##### <a name="return-values"></a>Valores devueltos

Siempre devuelve S_OK.
  
## <a name="enumerations"></a>Enumeraciones

CSISyncClient usa las enumeraciones siguientes.
  
### <a name="enum-lsceventsyncerrortype"></a>Enum LSCEventSyncErrorType
<a name="Enum_LSCEventSyncErrorType"> </a>

Esta enumeración especifica las categorías de errores que pueden producirse al sincronizar un archivo.
  
|Enumerator|Descripción|
|:-----|:-----|
|LSCEventSyncErrorType_UserInterventionRequiredUnexpected  <br/> |El error de sincronización de este evento fue inesperado y puede requerir una consideración especial. De forma predeterminada, es posible que el usuario tenga que intervenir.  <br/> |
|LSCEventSyncErrorType_NoInterventionRequired  <br/> |El error de sincronización de este evento no necesita una consideración especial. Office controlará automáticamente.  <br/> |
|LSCEventSyncErrorType_UserInterventionRequired  <br/> |El error de sincronización de este evento requiere que un usuario lo resuelva. Por ejemplo, el error de conflicto de combinación requiere que un usuario abra el documento y lo combine.  <br/> |
|LSCEventSyncErrorType_WaitingOnClient  <br/> |El error de sincronización de este evento requiere que el consumidor intervenga, pero no debe requerir una consideración especial por parte del usuario.  <br/> |
|LSCEventSyncErrorType_ClientInterventionRequired  <br/> |El error de sincronización de este evento requiere que el consumidor intervenga como caso especial.  <br/> |
|LSCEventSyncErrorType_Max  <br/> ||
   
### <a name="enum-lsceventtype"></a>Enum LSCEventType
<a name="Enum_LSCEventType"> </a>

Esta enumeración especifica el tipo de eventos que pueden producirse para un archivo determinado.
  
|Enumerator|Descripción|
|:-----|:-----|
|LSCEventType_None  <br/> ||
|LSCEventType_OnLocalChanges  <br/> |Se realizaron cambios en un archivo local.  <br/> |
|LSCEventType_OnOpenedByUser  <br/> |Un usuario abrió un archivo.  <br/> |
|LSCEventType_OnServerChangesDownloaded  <br/> |Ha terminado de descargar los cambios de archivo desde el servidor.  <br/> |
|LSCEventType_OnLocalChangesUploaded  <br/> |Ha terminado de cargar los cambios de archivo en el servidor.  <br/> |
|LSCEventType_OnLocalConflictStateChanged  <br/> |El estado de conflicto de combinación de un archivo ha cambiado.  <br/> |
|LSCEventType_OnFileAdded  <br/> |Se agregó un archivo.  <br/> |
|LSCEventType_OnFileDeleted  <br/> |Se eliminó un archivo.  <br/> |
|LSCEventType_OnSyncEnabled  <br/> |La sincronización se ha habilitado para los archivos de un usuario.  <br/> |
|LSCEventType_OnServerChangesDownloadStarted  <br/> |Inició la descarga de cambios de archivos desde el servidor.  <br/> |
|LSCEventType_OnLocalChangesUploadStarted  <br/> |Inició la carga de cambios de archivo en el servidor.  <br/> |
|LSCEventType_OnFilePathConflict  <br/> |Este evento se genera cuando una llamada a [ILSCLocalSyncClient::LocalFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange), [ILSCLocalSyncClient::ServerFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange)o [ILSCLocalSyncClient::RenameFile](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) provoca una colisión de ruta de acceso web o ruta de acceso local con otro archivo en la memoria caché de archivos de Office.  <br/> |
|LSCEventType_OnFileForked  <br/> ||
|LSCEventType_Max  <br/> ||
   
### <a name="enum-lsceventtypeoccurred"></a>Enum LSCEventTypeOccurred
<a name="Enum_LSCEventTypeOccurred"> </a>

Esta enumeración especifica el tipo de eventos que pueden producirse. El consumidor debe llamar a funciones específicas de ILSCLocalSyncClient en función del tipo de evento.
  
|Enumerator|Descripción|
|:-----|:-----|
|LSCEventTypeOccurred_GetChanges  <br/> |Se ha producido un EVENTO ILSC. El consumidor debe llamar a [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) para recuperar los datos.  <br/> |
|LSCEventTypeOccurred_GetSupportedFileExtensions  <br/> |Las extensiones de archivo compatibles han cambiado. El consumidor debe llamar a [ILSCLocalSyncClient::GetSupportedFileExtensions ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions) para recuperar la nueva lista de extensiones admitidas.  <br/> |
   
### <a name="enum-lscnetworksyncpermissiontype"></a>Enum LSCNetworkSyncPermissionType
<a name="Enum_LSCNetworkSyncPermissionType"> </a>

Esta enumeración especifica las marcas usadas para un costo heurístico de red. 

|Enumerator|Descripción|
|:-----|:-----|
|LSCNetworkSyncPermissionType_HighCost  <br/> |True si se invalida el costo heurístico de las redes costosas (como 3G).  <br/> |
|LSCNetworkSyncPermissionType_HighPowerUsage  <br/> |True si se invalida el costo heurístico para el uso de energía (como una batería).  <br/> |
   
### <a name="enum-lscstatusflag"></a>Enum LSCStatusFlag
<a name="Enum_LSCStatusFlag"> </a>

Esta enumeración se usa para representar el estado de sincronización de un archivo. 
  
|Enumerator|Descripción|
|:-----|:-----|
|LCSStatusFlag_None  <br/> ||
|LSCStatusFlag_UploadPending  <br/> |True si hay datos pendientes que enviar al archivo del servidor.  <br/> |
|LSCStatusFlag_DownloadPending  <br/> |True si hay datos pendientes que descargar del archivo del servidor.  <br/> |
|LSCStatusFlag_LocalFileUnchanged  <br/> |True si los datos Office en el archivo en su caché es la copia más reciente de los datos en el disco.  <br/> |
   

