---
title: Uso de CSISyncClient para controlar la caché de documentos de Office (ODC)
manager: soliver
ms.date: 07/13/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 394b8e6f-9132-4c98-8fd6-46ad3c871440
description: Obtenga información sobre cómo usar CSISyncClient para controlar la caché de documentos de Office (ODC).
ms.openlocfilehash: ce33063f88492bcd6f9682a4a6431fb36f138d55
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346259"
---
# <a name="using-csisyncclient-to-control-the-office-document-cache-odc"></a>Uso de CSISyncClient para controlar la caché de documentos de Office (ODC)

Obtenga información sobre cómo usar CSISyncClient para controlar la caché de documentos de Office (ODC).
  
CSISyncClient es un servidor COM fuera de proceso (CsiSyncClient. exe) que permite que Microsoft OneDrive controle el comportamiento de la caché de documentos de Office (ODC). Por ejemplo, OneDrive puede llamar a la ODC a través de CSISyncClient para cargar y descargar archivos en extremos habilitados de MS-FSSHTTP. Esto permite características avanzadas de seguridad del servicio de Office, como la co-autoría y las transiciones sin conexión a la línea.
  
CsiSyncClient está disponible en el escritorio de Office (tanto x86 como x64). Nota: aunque las versiones más recientes de Office pueden incluir CsiSyncClient, el proceso se usará solo para compatibilidad con versiones anteriores. La interfaz CsiSyncClient y la metodología para controlar el ODC cambiarán en futuras versiones de Office.
  
Actualmente, el identificador de clase está configurado para responder solo a OneDrive.
  
El objeto COM se puede usar como un servidor COM fuera de proceso y se ejecuta en CsiSyncClient. exe. Debido a las limitaciones de acceso (que usa la ODC), se suministra con el tipo de bit en el que se encuentra Office, por lo que Office x64 significa un objeto COM de x64 o una oficina x86 significa un objeto COM x86. Para superar esta limitación, especificar CLSCTX_LOCAL_SERVER como parte de CoCreateInstance tendrá el objeto COM hospedado como un servidor COM fuera de proceso, lo que permite la compatibilidad entre bits.
  
## <a name="interfaces"></a>Interfaces

CSISyncClient usa las siguientes interfaces.
  
### <a name="interface-ilsclocalsyncclient"></a>Interfaz ILSCLocalSyncClient

Esta es la interfaz principal que se usa para sincronizar archivos en Office.
  
- ProgID: Office. LocalSyncClient
- CLSID: {14286318-B6CF-49a1-81FC-D74AD94902F9}
- TypeLib: {66CDD37F-D313-4e81-8C31-4198F3E42C3C}
   
El objeto COM expuesto se usa como un servidor fuera de proceso. La especificación de CLSCTX_LOCAL_SERVER como parte de CoCreateInstance permite la compatibilidad entre procesos de 64 bits y 32 bits.
  
Una vez que haya creado conjuntamente el objeto COM, debe llamar a [ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) primero. Una vez que [ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) se haya completado correctamente, puede llamar a cualquier API tan a menudo como desee y en cualquier orden. También puede llamar a [ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) en un objeto ya inicializado, pero esto no hace nada. 
  
Las excepciones del párrafo anterior son [ILSCLocalSyncClient:: ResetCache](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) y [ILSCLocalSyncClient:: UnInitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize). Después de llamar a [ILSCLocalSyncClient:: UnInitialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) en el objeto com, debe destruir ese objeto y crear uno nuevo. [ILSCLocalSyncClient:: ResetCache](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) eliminará la subcaché, eliminará toda la información de archivo asociada en la memoria caché, pero dejará los documentos en el disco. También deja el estado intacto para comunicarse con la memoria caché. Esto le permite llamar de nuevo a [ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) para crear una nueva memoria caché sin tener que destruir y volver a crear el objeto com. 
  
**Funciones miembro públicas**

#### <a name="ilsclocalsyncclientdeletefile"></a>ILSCLocalSyncClient::D eleteFile

Se usa DeleteFile para quitar la información de archivo de la memoria caché. Sin embargo, este método dejará el archivo asociado en el disco y en el servidor.
  
`HRESULT ILSCLocalSyncClient::DeleteFile ([in] BSTR bstrResourceID)`

##### <a name="parameters"></a>Parameters

 _bstrResourceID_
  
La cadena que identifica el ResourceID del archivo. Este valor no debe estar vacío con un máximo de 128 caracteres. 
  
##### <a name="return-values"></a>Valores devueltos

|Valor|Descripción|
|:-----|:-----|
|E_FAIL  <br/> |La llamada ha fallado.  <br/> |
|E_INVALIDARG  <br/> |Uno o más parámetros no son válidos.  <br/> |
|E_FAIL  <br/> |La llamada ha fallado.  <br/> |
|E_LSC_FILENOTFOUND  <br/> |El ResourceID dado no está en la memoria caché.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |La inicialización no se ha llamado correctamente en el pasado.  <br/> |
|E_LSC_PENDINGCHANGESINCACHE  <br/> |El archivo está sincronizándose o abierto actualmente y no se puede eliminar.  <br/> |
|S_OK  <br/> |La llamada ha sido correcta.  <br/> |
   
#### <a name="ilsclocalsyncclientgetchanges"></a>ILSCLocalSyncClient:: GetChanges
<a name="ILSCLocalSyncClient_GetChanges"> </a>

GetChanges devuelve un enumerador de objetos ILSCEvent y también devuelve un token que se proporciona a la siguiente llamada a GetChanges, siempre que el cliente haya procesado el conjunto de eventos anterior. Los eventos antes de la _nPreviousChangesToken_ especificada se eliminarán y no estarán disponibles. Si no hay eventos que procesar, _pnCurrentChangesToken_ debe tener el mismo valor que _nPreviousChangesToken_, pero también se establecerá _ppiEvents_ . 
  
`HRESULT ILSCLocalSyncClient::GetChanges ([in] LONG nPreviousChangesToken, [out] LONG * pnCurrentChangesToken, [out] IEnumLSCEvent ** ppiEvents)`

##### <a name="parameters"></a>Parameters

 _nPreviousChangesToken_
  
Identifica qué evento fue procesado por última vez por el consumidor. 
  
 _pnCurrentChangesToken_
  
Identifica el evento más reciente que se entrega al consumidor. No debe ser nulo.
  
 _ppiEvents_
  
Un enumerador para los eventos entregados al consumidor. No debe ser nulo. 
  
##### <a name="return-values"></a>Valores devueltos

|Valor|Descripción|
|:-----|:-----|
|E_FAIL  <br/> |La llamada ha fallado.  <br/> |
|E_INVALIDARG  <br/> |Uno o más parámetros no son válidos.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) no se ha llamado correctamente en el pasado.  <br/> |
|S_OK  <br/> |La llamada ha sido correcta.  <br/> |
   
#### <a name="ilsclocalsyncclientgetclientnetworksyncpermission"></a>ILSCLocalSyncClient:: GetClientNetworkSyncPermission

GetClientNetworkSyncPermission se usa para consultar si se invalidan las heurísticas de sincronización de red de Office para el costo de red y el uso de energía. Cuando se está en una red 3G u otra red de alto coste, o cuando se ejecuta en una batería en lugar de estar enchufada, Office puede optar por bloquear el tráfico de red hasta un momento más oportuno.
  
`HRESULT ILSCLocalSyncClient::GetClientNetworkSyncPermission ([in] LSCNetworkSyncPermissionType nspType, [out] VARIANT_BOOL * pfSyncEnabled)`

##### <a name="parameters"></a>Parameters

 _nspType_
  
Marca que define el análisis heurístico de costo que se va a consultar. Vea [enumeraCión LSCNetworkSyncPermissionType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType). 
  
 _pfSyncEnabled_
  
Especifica si la heurística de costos solicitada está actualmente invalidada o no. No debe ser nulo. 
  
##### <a name="return-values"></a>Valores devueltos

|Valor|Descripción|
|:-----|:-----|
|E_FAIL  <br/> |La llamada ha fallado.  <br/> |
|E_INVALIDARG  <br/> |Uno o más parámetros no son válidos.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) no se ha llamado correctamente en el pasado.  <br/> |
|S_OK  <br/> |La llamada ha sido correcta.  <br/> |
   
#### <a name="ilsclocalsyncclientgetfilestatus"></a>ILSCLocalSyncClient:: GetFileStatus

GetFileStatus se usa para recopilar información de un archivo específico: si existe en la memoria caché, si está pendiente de comunicación con la copia del servidor, y si Office 2013 tiene los datos más actualizados de la copia local. Requiere una marca bit a bit de valores [LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag) de enumeración para determinar qué información debe consultar el objeto com CsiSyncClient. 
  
`HRESULT ILSCLocalSyncClient::GetFileStatus ([in] BSTR bstrResourceID, [in] LSCStatusFlag sfRequestedStatus, [out] BSTR * pbstrFileSystemPath, [out] BSTR * pbstrETag, [out] LSCStatusFlag * psfFileStatus)`

##### <a name="parameters"></a>Parameters

 _bstrResourceID_
  
La cadena que identifica el archivo en el cliente. Este valor no debe estar vacío, con un máximo de 128 caracteres. 
  
 _sfRequestedStatus_
  
Marca que define la información que se va a devolver. Vea [enumeraCión LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag). 
  
 _pbstrFileSystemPath_
  
La cadena que identifica la ubicación del archivo identificado por _bstrResourceID_ en el cliente. No debe ser nulo. 
  
 _pbstrETag_
  
Una cadena que contendrá la eTag para el archivo identificado por _bstrResourceID_. No debe ser nulo. 
  
 _psfFileStatus_
  
Una marca que contendrá el estado solicitado a través de _sfRequestedStatus_ para el archivo identificado por _bstrResourceID_. No debe ser nulo. Vea [enumeraCión LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag). 
  
##### <a name="return-values"></a>Valores devueltos

|Valor|Descripción|
|:-----|:-----|
|E_FAIL  <br/> |La llamada ha fallado.  <br/> |
|E_INVALIDARG  <br/> |Uno o más parámetros no son válidos.  <br/> |
|E_LSC_FILENOTFOUND  <br/> |La información de archivo especificada por _bstrResourceID_ no existe en la memoria caché.  <br/> |
|E_LSC_LOCALFILEUNAVAILABLE  <br/> |Se ha solicitado LSCStatusFlag_LocalFileUnchanged o el archivo especificado por _bstrResourceID_ está bloqueado o no se encuentra.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) no se ha llamado correctamente en el pasado.  <br/> |
|S_OK  <br/> |La llamada ha sido correcta.  <br/> |
   
#### <a name="ilsclocalsyncclientgetsupportedfileextensions"></a>ILSCLocalSyncClient:: GetSupportedFileExtensions
<a name="ILSCLocalSyncClient_GetSupportedFileExtensions"> </a>

GetSupportedFileExtensions devuelve una lista de extensiones de archivo delimitadas por canalización que son compatibles actualmente con el objeto COM CsiSyncClient. Tenga en cuenta que esta lista puede cambiar y que se notificará al consumidor un cambio a través del objeto IPartnerActivityCallback proporcionado en [ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) (vea EventOccured). 
  
Un ejemplo de la cadena devuelta es el siguiente: "| docx | docm | pptx |"
  
`HRESULT ILSCLocalSyncClient::GetSupportedFileExtensions ([out] BSTR * pbstrSupportedFileExtensions)`

##### <a name="parameters"></a>Parameters

 _pbstrSupportedFileExtensions_
  
Una cadena que se va a establecer con un conjunto de extensiones de archivo delimitadas por canalización que admite el objeto COM CsiSyncClient. No debe ser nulo. 
  
##### <a name="return-values"></a>Valores devueltos

|Valor|Descripción|
|:-----|:-----|
|E_FAIL  <br/> |La llamada ha fallado.  <br/> |
|E_INVALIDARG  <br/> |Uno o más parámetros no son válidos.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) no se ha llamado correctamente en el pasado.  <br/> |
|S_OK  <br/> |La llamada ha sido correcta.  <br/> |
   
#### <a name="ilsclocalsyncclientinitialize"></a>ILSCLocalSyncClient:: Initialize
<a name="ILSCLocalSyncClient_Initialize"> </a>

Initialize debe ser el primer método al que se llama. De lo contrario, todas las demás API devolverán E_LSC_NOTINITIALIZED. Al llamar a Initialize en un objeto que ya se ha inicializado, se devuelve S_OK y no se realiza ninguna acción. Si se devuelve E_LSC_CACHEMISMATCH, el autor de la llamada puede llamar a [ILSCLocalSyncClient:: ResetCache](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) para eliminar la memoria caché asociada con el SuppliedID dado. Sin embargo, en este caso otras API seguirán devolviendo E_LSC_NOTINITIALIZED. 
  
`HRESULT ILSCLocalSyncClient::Initialize ([in] BSTR bstrSuppliedID, [in] BSTR bstrProgID, [in] BSTR bstrFileSystemDirectoryHint, [in] IPartnerActivityCallback * pEventCallback, [out] VARIANT_BOOL * pfCreatedNewCache)`

##### <a name="parameters"></a>Parameters

 _bstrSuppliedID_
  
Identifica el consumidor y la caché que se va a usar. No debe estar vacío con un máximo de 32 caracteres. 
  
 _bstrProgID_
  
Identifica el objeto COM del consumidor para la comunicación bidireccional. No debe estar vacío con un máximo de 39 caracteres. Vea [ \<la\> clave ProgID](https://docs.microsoft.com/windows/desktop/com/-progid--key) para obtener más información sobre los ProgID. 
  
 _bstrFileSystemDirectoryHint_
  
Identifica la raíz del directorio en el que se almacenarán los archivos locales. No debe estar vacío con un máximo de 256 caracteres. El directorio ya debe existir. 
  
 _pEventCallback_
  
La interfaz de devolución de llamada a la que CsiSyncClient se notificarán los cambios. Vea IPartnerActivityCallback:: EventOccurred. Este valor no debe ser nulo. 
  
 _pfCreatedNewCache_
  
Devuelve si se creó una nueva memoria caché. Si no hay ninguna memoria caché asociada con SuppliedID, se creará una. Este valor no debe ser nulo.
  
##### <a name="return-values"></a>Valores devueltos

|Valor|Descripción|
|:-----|:-----|
|E_FAIL  <br/> |La llamada ha fallado.  <br/> |
|E_INVALIDARG  <br/> |Uno o más parámetros no son válidos.  <br/> |
|E_LSC_CACHEMISMATCH  <br/> |Un SuppliedID ya tiene una memoria caché asociada, pero tiene un ProgId o FileSystemDirectoryHint diferente de los que se proporcionan.  <br/> |
|E_LSC_DIRECTORYHINTCONFLICT  <br/> |El FileSystemDirectoryHint (o una subcarpeta) ya existe en una memoria caché diferente.  <br/> |
|E_LAC_PROGIDCONFLICT  <br/> |El ProgID ya existe en una memoria caché diferente.  <br/> |
|S_OK  <br/> |La llamada ha sido correcta.  <br/> |
   
#### <a name="ilsclocalsyncclientlocalfilechange"></a>ILSCLocalSyncClient:: LocalFileChange
<a name="ILSCLocalSyncClient_LocalFileChange"> </a>

LocalFileChange se usa para indicarle al objeto CsiSyncClient COM que intente cargar el archivo especificado. El método preparará el archivo que se va a cargar, incluida la lectura del contenido actual del archivo. Si ya hay una carga pendiente, se descartará la carga anterior y se preparará el contenido nuevo para la carga. Si el archivo está abierto para editarlo en una aplicación, este método devolverá S_OK sin preparar el archivo para la carga (la aplicación ya debe realizar este paso si hay cambios).
  
Este método permite las cargas si se marcaron como bloqueadas anteriormente (vea [ILSCLocalSyncClient:: RenameFile ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile)).
  
`HRESULT ILSCLocalSyncClient::LocalFileChange ([in] BSTR bstrFileSystemPath, [in] BSTR bstrWebPath, [in] BSTR bstrResourceID)`

##### <a name="parameters"></a>Parameters

 _bstrFileSystemPath_
  
Una cadena que identifica el archivo en el cliente. Este valor debe ser una ruta de acceso local no vacía con un máximo de 256 caracteres. Esta ruta de acceso debe estar en el árbol de directorios especificado por FileSystemDirectoryHint cuando se realizó la llamada a [ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) . 
  
 _bstrResourceID_
  
Una cadena que identifica el ResourceID del archivo. Este valor no debe estar vacío con un máximo de 128 caracteres. 
  
 _bstrWebPath_
  
Una cadena que identifica el archivo en el servidor. Este valor no debe estar vacío, es una dirección URL válida, pero no puede ser superior a INTERNET_MAX_URL_LENGTH https://support.microsoft.com/kb/208427, según se define en. 
  
##### <a name="return-values"></a>Valores devueltos

|Valor|Descripción|
|:-----|:-----|
|E_FAIL  <br/> |La llamada ha fallado.  <br/> |
|E_INVALIDARG  <br/> |Uno o más parámetros no son válidos.  <br/> |
|E_LSC_CONFLICTINGFILE  <br/> |El archivo especificado por _bstrFileSystemPath_ tiene un ResourceID diferente del especificado. Cuando se devuelve este error, se envía un evento de tipo LSCEventType_OnFilePathConflict. Vea [ILSCLocalSyncClient:: GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges).  <br/> |
|E_LSC_FILENOTFOUND  <br/> |El archivo se eliminó a medio funcionamiento.  <br/> |
|E_LSC_FILENOTSUPPORTED  <br/> |La extensión de archivo dada no es compatible con el objeto COM CsiSyncClient. Vea [ILSCLocalSyncClient:: GetSupportedFileExtensions ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions).  <br/> |
|E_LSC_FILEUPTODATE  <br/> |El objeto COM no programó una carga porque el archivo de la memoria caché tenía los cambios más recientes del disco.  <br/> |
|E_LSC_LOCALFILEUNAVAILABLE  <br/> |El archivo especificado por _bstrFileSystemPath_ falta o está bloqueado.  <br/> |
|E_LSC_LOCALPATHNOTMAPPED  <br/> |El FileSystemPath especificado no está en la raíz del directorio especificada por FileSystemDirectoryHint cuando se realizó la llamada a Initialize.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) no se ha llamado correctamente en el pasado.  <br/> |
|E_LSC_PATHMISMATCH  <br/> |El archivo especificado por _bstrResourceID_ tiene un FileSystemPath diferente del especificado.  <br/> |
|E_LSC_PENDINGCHANGESINCACHE  <br/> |El archivo especificado ya tiene cambios pendientes en una memoria caché diferente y todavía no se puede asociar a la memoria caché del cliente.  <br/> |
|E_LSC_SERVERPATHINDIFFERENTCACHE  <br/> |La webPath proporcionada se encuentra en una memoria caché diferente.  <br/> |
|S_OK  <br/> |La llamada ha sido correcta.  <br/> |
   
#### <a name="ilsclocalsyncclientrenamefile"></a>ILSCLocalSyncClient:: RenameFile
<a name="ILSCLocalSyncClient_RenameFile"> </a>

RenameFile asociará una nueva dirección URL y una ruta de acceso local para un ResourceID determinado. Si el archivo especificado por el ResourceID no existe todavía en la memoria caché, se intentará crearlo y marcarlo para su descarga.
  
`HRESULT ILSCLocalSyncClient::RenameFile ([in] BSTR bstrResourceID, [in] BSTR bstrNewFileSystemPath, [in] BSTR bstrNewWebPath, [in] VARIANT_BOOL fBlockUploads)`

##### <a name="parameters"></a>Parameters

 _bstrResourceID_
  
Una cadena que identifica el ResourceID del archivo. Este valor no debe estar vacío con un máximo de 128 caracteres. 
  
 _bstrNewFileSystemPath_
  
Una cadena que especifica la nueva ruta de acceso local para el archivo. Este valor debe ser una ruta de acceso local no vacía con un máximo de 256 caracteres. Esta ruta de acceso debe estar en el árbol de directorios especificado por FileSystemDirectoryHint cuando se realizó la llamada a Initialize. 
  
 _bstrNewWebPath_
  
Una cadena que especifica la nueva dirección URL para el archivo. Este valor debe ser una dirección URL válida no vacía, pero no puede ser superior a INTERNET_MAX_URL_LENGTH, https://support.microsoft.com/kb/208427como se define en. 
  
 _fBlockUploads_
  
Especifica si se permite actualmente la carga a la nueva ubicación. 
  
##### <a name="return-values"></a>Valores devueltos

|Valor|Descripción|
|:-----|:-----|
|E_FAIL  <br/> |La llamada ha fallado.  <br/> |
|E_INVALIDARG  <br/> |Uno o más parámetros no son válidos.  <br/> |
|E_LSC_CONFLICTINGFILE  <br/> |_BstrNewFileSystemPath_ o _bstrNewWebPath_ ya existen en otro archivo en cualquier caché. Cuando se devuelve este error, se envía un evento de tipo LSCEventType_OnFilePathConflict. Vea [ILSCLocalSyncClient:: GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges).  <br/> |
|E_LSC_FILENOTFOUND  <br/> |La información del archivo se eliminó de la memoria caché mientras se ejecutaba este método.  <br/> |
|E_LSC_LOCALPATHNOTMAPPED  <br/> |El FileSystemPath especificado no está en la raíz del directorio especificada por FileSystemDirectoryHint cuando se realizó la llamada a Initialize.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) no se ha llamado correctamente en el pasado.  <br/> |
|E_LSC_PENDINGCHANGESINCACHE  <br/> |El archivo especificado está sincronizándose actualmente en una aplicación de Office.  <br/> |
|S_OK  <br/> |La llamada ha sido correcta.  <br/> |
   
#### <a name="ilsclocalsyncclientresetcache"></a>ILSCLocalSyncClient:: ResetCache
<a name="ILSCLocalSyncClient_ResetCache"> </a>

ResetCache eliminará la memoria caché asociada con el SuppliedID que se proporcionó al inicializar. Esto incluye toda la información del archivo, pero dejará los archivos en el cliente y en el servidor. Este método también deja el objeto en un estado parcialmente sin inicializar. Las únicas llamadas válidas después de esto son [ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) o [ILSCLocalSyncClient:: UnInitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize). Se puede llamar a este método si se produce un error en la inicialización y se devuelve E_LSC_CACHEMISMATCH, y se elimina la memoria caché asociada con el SuppliedID que se proporcionó con la llamada failed.
  
`HRESULT ILSCLocalSyncClient::ResetCache()`

##### <a name="parameters"></a>Parameters

Ninguno
  
##### <a name="return-values"></a>Valores devueltos

|Valor|Descripción|
|:-----|:-----|
|E_FAIL  <br/> |La llamada ha fallado.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) no se llamó correctamente en el pasado.  <br/> |
|S_OK  <br/> |La llamada ha sido correcta.  <br/> |
   
#### <a name="ilsclocalsyncclientserverfilechange"></a>ILSCLocalSyncClient:: ServerFileChange
<a name="ILSCLocalSyncClient_ServerFileChange"> </a>

ServerFileChange indica al objeto COM CsiSyncClient que debe marcar el archivo especificado para la descarga. Si el archivo está abierto en una aplicación de Office para su edición, este método devolverá S_OK sin marcar el archivo que se va a descargar (la aplicación ya debe realizar este paso si hay cambios).
  
Este método permitirá las descargas si se marcó como bloqueada anteriormente (vea RenameFile).
  
`HRESULT ILSCLocalSyncClient::ServerFileChange ([in] BSTR bstrFileSystemPath, [in] BSTR bstrWebPath, [in] BSTR bstrResourceID)`

##### <a name="parameters"></a>Parámetros

|Parameter|Descripción|
|:-----|:-----|
|bstrFileSystemPath  <br/> |Una cadena que identifica el archivo en el cliente. Este valor debe ser una ruta de acceso local no vacía con un máximo de 256 caracteres. Esta ruta de acceso debe estar en el árbol de directorios especificado por FileSystemDirectoryHint cuando se realizó la llamada a Initialize.  <br/> |
|bstrResourceID  <br/> |Una cadena que identifica el ResourceID del archivo. Este valor no debe estar vacío con un máximo de 128 caracteres.  <br/> |
|bstrWebPath  <br/> |Una cadena que identifica el archivo en el servidor. Este valor debe ser una dirección URL válida no vacía, pero no puede ser superior a INTERNET_MAX_URL_LENGTH, como https://support.microsoft.com/kb/208427se define en.  <br/> |
   
##### <a name="return-values"></a>Valores devueltos

|Valor|Descripción|
|:-----|:-----|
|E_FAIL  <br/> |Error al establecer el estado de conectividad de caché.  <br/> |
|E_LSC_CONFLICTINGFILE  <br/> |El archivo especificado por _bstrFileSystemPath_ tiene un ResourceID diferente del especificado.  <br/> |
|E_LSC_FILENOTSUPPORTED  <br/> |La extensión de archivo dada no es compatible con el objeto COM CsiSyncClient. Consulte GetSupportedFileExtensions.  <br/> |
|E_LSC_FILENOTFOUND  <br/> |El archivo se eliminó en Mid-Operation.  <br/> |
|E_INVALIDARG  <br/> |Uno o más parámetros no son válidos.  <br/> |
|E_LSC_LOCALPATHNOTMAPPED  <br/> |El FileSystemPath especificado no está en la raíz del directorio especificada por FileSystemDirectoryHint cuando se realizó la llamada a Initialize.  <br/> |
|E_LSC_NOINITIALIZED  <br/> |[ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) no se ha llamado correctamente en el pasado.  <br/> |
|E_LSC_PATHMISMATCH  <br/> |El archivo especificado por _bstrResourceID_ tiene un FileSystemPath diferente del especificado.  <br/> |
|E_LSC_PENDINGCHANGESINCACHE  <br/> |El archivo especificado ya tiene cambios pendientes en una memoria caché diferente y todavía no se puede asociar a la memoria caché del cliente.  <br/> |
|E_LSC_SERVERPATHINDIFFERENTCACHE  <br/> |La webPath proporcionada se encuentra en una memoria caché diferente.  <br/> |
|S_OK  <br/> |La llamada ha sido correcta.  <br/> |
   
#### <a name="ilsclocalsyncclientsetclientconnectivitystate"></a>ILSCLocalSyncClient:: SetClientConnectivityState
<a name="ILSCLocalSyncClient_ServerFileChange"> </a>

Establece la caché en un estado en línea o sin conexión. Si está sin conexión, Office no intentará comunicarse con el servidor en busca de archivos en dicha memoria caché, independientemente de la configuración de _fBlockUploads_ de cada archivo individual. 
  
`HRESULT ILSCLocalSyncClient::SetClientConnectivityState ([in] VARIANT_BOOL fIsOnline)`

##### <a name="parameters"></a>Parameters

 _fIsOnline_
  
Un valor booleano que determina el estado de conectividad de la memoria caché. 
  
##### <a name="return-values"></a>Valores devueltos

|Valor|Descripción|
|:-----|:-----|
|E_FAIL  <br/> |Error al establecer el estado de conectividad de caché.  <br/> |
|E_INVALIDARG  <br/> |Uno o más parámetros no son válidos.  <br/> |
|E_LSC_NOINITIALIZED  <br/> |[ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) no se ha llamado correctamente en el pasado.  <br/> |
|S_OK  <br/> |La llamada ha sido correcta.  <br/> |
   
#### <a name="ilsclocalsyncclientsetclientnetworksyncpermission"></a>ILSCLocalSyncClient:: SetClientNetworkSyncPermission
<a name="ILSCLocalSyncClient_ServerFileChange"> </a>

SetClientNetworkSyncPermission se usa para invalidar o restoreOffice heurística de sincronización del costo de red y el uso de energía. Cuando se está en una red 3G u otra red de alto coste, o cuando se ejecuta en una batería en lugar de estar enchufada, Office puede optar por bloquear el tráfico de red hasta un momento más oportuno. El consumidor de esta API puede usarla para reemplazar las heurísticas de Office y forzar la sincronización para que se produzcan.
  
`HRESULT ILSCLocalSyncClient::SetClientNetworkSyncPermission ([in] LSCNetworkSyncPermissionType nspType, [in] VARIANT_BOOL fEnableSync)`

##### <a name="parameters"></a>Parameters

 _nspType_
  
Marca que define el análisis heurístico que se va a reemplazar. Vea [enumeraCión LSCNetworkSyncPermissionType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType).
  
 _fEnableSync_
  
Especifica si se debe forzar la sincronización en, por lo que se invalida el análisis heurístico o ya no se reemplaza. 
  
##### <a name="return-values"></a>Valores devueltos

|Valor|Descripción|
|:-----|:-----|
|E_FAIL  <br/> |Error al reemplazar la heurística de sincronización.  <br/> |
|E_LSC_NOINITIALIZED  <br/> |[ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) no se ha llamado correctamente en el pasado.  <br/> |
|S_OK  <br/> |La llamada ha sido correcta.  <br/> |
   
#### <a name="ilsclocalsyncclientuninitialize"></a>ILSCLocalSyncClient:: UnInitialize
<a name="ILSCLocalSyncClient_Uninitialize"> </a>

Descarga la memoria caché del objeto COM y realiza operaciones de cierre. [ILSCLocalSyncClient:: UnInitialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) Se debe llamar antes de destruir el objeto COM. Una vez que se llama a no se puede llamar a ninguna otra API, se debe destruir el objeto COM y crear uno nuevo si desea continuar operaciones. 
  
`HRESULT ILSCLocalSyncClient::Uninitialize ()`

##### <a name="parameters"></a>Parámetros

Ninguno.
  
##### <a name="return-values"></a>Valores devueltos

|Valor|Descripción|
|:-----|:-----|
|E_FAIL  <br/> |Error al inicializar.  <br/> |
|E_LSC_NOINITIALIZED  <br/> |[ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) no se ha llamado correctamente en el pasado.  <br/> |
|S_OK  <br/> |La llamada ha sido correcta.  <br/> |
   
### <a name="interface-ienumlscevent"></a>Interfaz IEnumLSCEvent

Esta interfaz representa una lista de eventos ILSCEvent.
  
**Funciones miembro públicas**

#### <a name="ienumlsceventfnext"></a>IEnumLSCEvent:: FNext

Recupera el siguiente evento de la lista de eventos.
  
`HRESULT IEnumLSCEvent::FNext ([out] ILSCEvent ** ppiLSCEvent)`

##### <a name="parameters"></a>Parameters

 _ppiLSCEvent_
  
Un puntero a una interfaz ILSCEvent.
  
##### <a name="return-values"></a>Valores devueltos

|Valor|Descripción|
|:-----|:-----|
|E_FAIL  <br/> |No hay más eventos.  <br/> |
|S_OK  <br/> |La llamada se realizó correctamente.  <br/> |
   
#### <a name="ienumlsceventreset"></a>IEnumLSCEvent:: RESET

Restablece el enumerador al primer evento.
  
`HRESULT IEnumLSCEvent::Reset ()`

##### <a name="parameters"></a>Parámetros

Ninguno.
  
##### <a name="return-values"></a>Valores devueltos

Siempre Devuelve S_OK. 
  
### <a name="interface-ilscevent"></a>Interfaz ILSCEvent

Esta interfaz representa un evento Synchronizing. Toda la información sobre el evento se puede recuperar desde la interfaz.
  
**Funciones miembro públicas**

#### <a name="ilsceventgetconflictstatus"></a>ILSCEvent:: GetConflictStatus

Tenga en cuenta que este valor se rellena cuando se llama a [ILSCLocalSyncClient:: GetChanges](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) , no cuando se creó el evento, por lo que solo tendrá el estado actual del archivo, no el estado del archivo cuando el estado del conflicto haya cambiado. 
  
Este valor solo se rellena cuando la [enumeraCión LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) del evento es LSCEventType_OnLocalConflictStateChanged. 
  
`HRESULT ILSCEvent::GetConflictStatus ([out] VARIANT_BOOL * pfIsInConflict)`

##### <a name="parameters"></a>Parameters

 _pfIsInConflict_
  
El estado de conflicto actual del archivo asociado al evento.
  
##### <a name="return-values"></a>Valores devueltos

Siempre Devuelve S_OK. 
  
#### <a name="ilsceventgeterror"></a>ILSCEvent:: GetError

Este valor solo se rellena cuando la [enumeraCión LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) del evento es LSCEventType_OnServerChangesDownloaded o LSCEventType_OnLocalChangesUploaded. 
  
`HRESULT ILSCEvent::GetError ([out] LONG * pnError)`

##### <a name="parameters"></a>Parameters

 _pnError_
  
Error asociado a este evento.
  
##### <a name="return-values"></a>Valores devueltos

Siempre Devuelve S_OK. 
  
#### <a name="ilsceventgetetag"></a>ILSCEvent:: GetETag

Este valor solo se rellena cuando la [enumeraCión LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) del evento es LSCEventType_OnServerChangesDownloaded o LSCEventType_OnLocalChangesUploaded. 
  
`HRESULT ILSCEvent::GetETag ([out] BSTR * pbstrETag)`

##### <a name="parameters"></a>Parameters

 _pbstrETag_
  
ETag asociado a este evento
  
##### <a name="return-values"></a>Valores devueltos

Siempre Devuelve S_OK. 
  
#### <a name="ilsceventgeteventtype"></a>ILSCEvent:: GetEventType

Obtiene el tipo de este evento.
  
`HRESULT ILSCEvent::GetEventType ([out] LSCEventType * pnEventType)`

##### <a name="parameters"></a>Parameters

 _pnEventType_
  
El tipo de evento de este evento. Consulte la [enumeraCión LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) para valores válidos. No debe ser nulo. 
  
##### <a name="return-values"></a>Valores devueltos

|Valor|Descripción|
|:-----|:-----|
|E_INVALIDARG  <br/> |Uno o más parámetros no son válidos.  <br/> |
|S_OK  <br/> |La llamada se realizó correctamente.  <br/> |
   
#### <a name="ilsceventgetlocalworkingpath"></a>ILSCEvent:: GetLocalWorkingPath

Obtiene la ruta de trabajo local de este evento.
  
`HRESULT ILSCEvent::GetLocalWorkingPath ([out] BSTR * pbstrLocalWorkingPath)`

##### <a name="parameters"></a>Parameters

 _pbstrLocalWorkingPath_
  
Ruta de acceso local del archivo al que pertenece este evento. 
  
##### <a name="return-values"></a>Valores devueltos

Siempre Devuelve S_OK. 
  
#### <a name="ilsceventgetresourceid"></a>ILSCEvent:: GetResourceID

Obtiene el identificador de recurso para el evento.
  
`HRESULT ILSCEvent::GetResourceID ([out] BSTR * pbstrResourceID)`

##### <a name="parameters"></a>Parameters

 _pbstrResourceID_
  
ResourceID del archivo asociado a este evento.
  
##### <a name="return-values"></a>Valores devueltos

Siempre Devuelve S_OK. 
  
#### <a name="ilsceventgetresourceidattempted"></a>ILSCEvent:: GetResourceIDAttempted

Este valor solo se rellena cuando la [enumeraCión LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) del evento es LSCEventType_OnFilePathConflict. Cuando una llamada a [ILSCLocalSyncClient:: LocalFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange), [ILSCLocalSyncClient:: ServerFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange)o [ILSCLocalSyncClient:: RenameFile](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) daría lugar a una ruta de acceso web o a una colisión de ruta de acceso local con otro archivo en la memoria caché de archivos de Office, este se genera el evento. 
  
`HRESULT ILSCEvent::GetResourceIDAttempted ([out] BSTR * pbstrResourceIDAttempted)`

##### <a name="parameters"></a>Parameters

 _pbstrResourceIDAttempted_
  
ResourceID que ha provocado la generación de este evento. No debe ser nulo. 
  
##### <a name="return-values"></a>Valores devueltos

Siempre Devuelve S_OK. 
  
#### <a name="ilsceventgetsyncerrortype"></a>ILSCEvent:: GetSyncErrorType

Este valor solo se rellena cuando la [enumeraCión LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) del evento es LSCEventType_OnServerChangesDownloaded o LSCEventType_OnLocalChangesUploaded. 
  
`HRESULT ILSCEvent::GetSyncErrorType ([out] LSCEventSyncErrorType * pnSyncErrorType)`

##### <a name="parameters"></a>Parameters

 _pnSyncErrorType_
  
El tipo de error asociado a este evento. Vea la [enumeraCión LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) para obtener valores potenciales. No debe ser nulo. 
  
##### <a name="return-values"></a>Valores devueltos

|Valor|Descripción|
|:-----|:-----|
|E_INVALIDARG  <br/> |Uno o más parámetros no son válidos.  <br/> |
|S_OK  <br/> |La llamada se realizó correctamente.  <br/> |
   
#### <a name="ilsceventgetwebpath"></a>ILSCEvent:: GetWebPath

Este valor solo se rellena cuando la [enumeraCión LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) del evento es LSCEventType_OnFilePathConflict. 
  
`HRESULT ILSCEvent::GetWebPath ([out] BSTR * pbstrWebPath)`

##### <a name="parameters"></a>Parameters

 _pbstrWebPath_
  
Especifica la ruta de acceso web asociada a este evento. No debe ser nulo. 
  
##### <a name="return-values"></a>Valores devueltos

Siempre Devuelve S_OK. 
  
### <a name="interface-ilscevent2"></a>Interfaz ILSCEvent2

Esta interfaz contiene información adicional acerca de un evento de sincronización.
  
**Funciones miembro públicas**

#### <a name="ilscevent2geterrorchain"></a>ILSCEvent2:: GetErrorChain

Obtiene la información de la cadena de errores sobre un evento de sincronización.
  
`HRESULT ILSCEvent2::GetErrorChain ([out] BSTR * pbstrErrorChain)`

##### <a name="parameters"></a>Parameters

 _pbstrErrorChain_
  
Una cadena que contenga la información de la cadena de errores. No debe ser nulo. 
  
##### <a name="return-values"></a>Valores devueltos

|Valor|Descripción|
|:-----|:-----|
|E_NOTIMPL  <br/> |La versión instalada de Office no es compatible con esta interfaz  <br/> |
|E_INVALIDARG  <br/> |Uno o varios de los valores de parámetro no son válidos.  <br/> |
|E_FAIL  <br/> |La información de la cadena de error no está disponible.  <br/> |
|S_OK  <br/> |La llamada se realizó correctamente.  <br/> |
   
### <a name="interface-ipartneractivitycallback"></a>Interfaz IPartnerActivityCallback

Esta interfaz proporciona una función de devolución de llamada al objeto COM CSISyncClient.
  
**Funciones miembro públicas**

#### <a name="ipartneractivitycallbackeventoccurred"></a>IPartnerActivityCallback:: EventOccurred

Se trata de una función de devolución de llamada en el objeto que se asigna al objeto COM CsiSyncClient. Se espera que cuando se produzca un evento (vea la [enumeraCión LSCEventTypeOccurred](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred) para tipos válidos de eventos), el objeto com CsiSyncClient llame a este método, señalando al consumidor. 
  
`HRESULT IPartnerActivityCallback::EventOccurred ([in] LSCEventTypeOccurred eEventTypeOccurred)`

##### <a name="parameters"></a>Parameters

 _eEventTypeOccurred_
  
El tipo de evento de este evento. Consulte la [enumeraCión LSCEventTypeOccurred](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred) para valores válidos. 
  
##### <a name="return-values"></a>Valores devueltos

Siempre Devuelve S_OK.
  
## <a name="enumerations"></a>Enumeraciones

CSISyncClient usa las siguientes enumeraciones.
  
### <a name="enum-lsceventsyncerrortype"></a>Enumeración LSCEventSyncErrorType
<a name="Enum_LSCEventSyncErrorType"> </a>

Esta enumeración especifica las categorías de errores que se pueden producir al sincronizar un archivo.
  
|Enumerador|Descripción|
|:-----|:-----|
|LSCEventSyncErrorType_UserInterventionRequiredUnexpected  <br/> |El error de sincronización de este evento fue inesperado y puede requerir una consideración especial. De forma predeterminada, es posible que el usuario tenga que intervenir.  <br/> |
|LSCEventSyncErrorType_NoInterventionRequired  <br/> |No es necesario tener en cuenta el error de sincronización de este evento. Office lo controlará automáticamente.  <br/> |
|LSCEventSyncErrorType_UserInterventionRequired  <br/> |El error de sincronización de este evento requiere que un usuario lo resuelva. Por ejemplo, el error de conflicto de combinación requiere que un usuario abra el documento y lo combine.  <br/> |
|LSCEventSyncErrorType_WaitingOnClient  <br/> |El error de sincronización de este evento requiere que el consumidor intervenga, pero el usuario no debe tener una consideración especial.  <br/> |
|LSCEventSyncErrorType_ClientInterventionRequired  <br/> |El error de sincronización de este evento requiere que el consumidor intervenga como caso especial.  <br/> |
|LSCEventSyncErrorType_Max  <br/> ||
   
### <a name="enum-lsceventtype"></a>Enumeración LSCEventType
<a name="Enum_LSCEventType"> </a>

Esta enumeración especifica el tipo de eventos que pueden producirse para un archivo determinado.
  
|Enumerador|Descripción|
|:-----|:-----|
|LSCEventType_None  <br/> ||
|LSCEventType_OnLocalChanges  <br/> |Se realizaron cambios en un archivo local.  <br/> |
|LSCEventType_OnOpenedByUser  <br/> |Un usuario abrió un archivo.  <br/> |
|LSCEventType_OnServerChangesDownloaded  <br/> |Terminó de descargar los cambios de archivo del servidor.  <br/> |
|LSCEventType_OnLocalChangesUploaded  <br/> |Se terminaron de cargar los cambios de archivo en el servidor.  <br/> |
|LSCEventType_OnLocalConflictStateChanged  <br/> |El estado de conflicto de combinación de un archivo ha cambiado.  <br/> |
|LSCEventType_OnFileAdded  <br/> |Se ha agregado un archivo.  <br/> |
|LSCEventType_OnFileDeleted  <br/> |Se ha eliminado un archivo.  <br/> |
|LSCEventType_OnSyncEnabled  <br/> |La sincronización se habilitó para los archivos de un usuario.  <br/> |
|LSCEventType_OnServerChangesDownloadStarted  <br/> |Se inició la descarga de cambios del archivo desde el servidor.  <br/> |
|LSCEventType_OnLocalChangesUploadStarted  <br/> |Se inició la carga de cambios de archivo en el servidor.  <br/> |
|LSCEventType_OnFilePathConflict  <br/> |Este evento se genera cuando una llamada a [ILSCLocalSyncClient:: LocalFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange), [ILSCLocalSyncClient:: ServerFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange)o [ILSCLocalSyncClient:: RenameFile](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) causa una ruta de acceso web o una colisión de ruta de acceso local con otro archivo en el Caché de archivos de Office.  <br/> |
|LSCEventType_OnFileForked  <br/> ||
|LSCEventType_Max  <br/> ||
   
### <a name="enum-lsceventtypeoccurred"></a>Enumeración LSCEventTypeOccurred
<a name="Enum_LSCEventTypeOccurred"> </a>

Esta enumeración especifica el tipo de eventos que pueden producirse. El consumidor debe llamar a funciones específicas de ILSCLocalSyncClient basadas en el tipo de evento.
  
|Enumerador|Descripción|
|:-----|:-----|
|LSCEventTypeOccurred_GetChanges  <br/> |Se ha producido un ILSCEvent. El consumidor debe llamar a [ILSCLocalSyncClient:: GetChanges](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) para recuperar los datos.  <br/> |
|LSCEventTypeOccurred_GetSupportedFileExtensions  <br/> |Las extensiones de archivo compatibles han cambiado. El consumidor debe llamar a [ILSCLocalSyncClient:: GetSupportedFileExtensions](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions) para recuperar la nueva lista de extensiones admitidas.  <br/> |
   
### <a name="enum-lscnetworksyncpermissiontype"></a>Enumeración LSCNetworkSyncPermissionType
<a name="Enum_LSCNetworkSyncPermissionType"> </a>

Esta enumeración especifica los indicadores usados para una heurística de costos de red. 

|Enumerador|Descripción|
|:-----|:-----|
|LSCNetworkSyncPermissionType_HighCost  <br/> |True si se invalida el análisis de costos para redes costosas (como 3G).  <br/> |
|LSCNetworkSyncPermissionType_HighPowerUsage  <br/> |True si se reemplaza el análisis heurístico del uso de energía (por ejemplo, una batería).  <br/> |
   
### <a name="enum-lscstatusflag"></a>Enumeración LSCStatusFlag
<a name="Enum_LSCStatusFlag"> </a>

Esta enumeración se usa para representar el estado de sincronización de un archivo. 
  
|Enumerador|Descripción|
|:-----|:-----|
|LCSStatusFlag_None  <br/> ||
|LSCStatusFlag_UploadPending  <br/> |True si hay datos pendientes para enviar al archivo del servidor.  <br/> |
|LSCStatusFlag_DownloadPending  <br/> |True si hay datos pendientes que descargar desde el archivo del servidor.  <br/> |
|LSCStatusFlag_LocalFileUnchanged  <br/> |True si la oficina de datos tiene en el archivo en su caché la copia más reciente de los datos en el disco.  <br/> |
   

