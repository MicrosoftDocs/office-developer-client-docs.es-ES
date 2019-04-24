---
title: Integración de aplicaciones de administración con Office 365 Installer de hacer clic y ejecutar
manager: kelbow
ms.date: 10/22/2017
ms.audience: ITPro
localization_priority: Normal
ms.assetid: c0fa8fed-1585-4566-a9be-ef6d6d1b4ce8
description: Obtenga información sobre cómo integrar el instalador de hacer clic y ejecutar de Office 365 con una solución de administración de software.
ms.openlocfilehash: cdcdde0618e2b96ce997ba5e263f75d85c21fd11
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318357"
---
# <a name="integrating-manageability-applications-with-office-365-click-to-run-installer"></a>Integración de aplicaciones de administración con Office 365 Installer de hacer clic y ejecutar

Obtenga información sobre cómo integrar el instalador de hacer clic y ejecutar de Office 365 con una solución de administración de software.
  
El instalador de hacer clic y ejecutar de Office 365 proporciona una interfaz COM que permite a los profesionales de ti y a las soluciones de administración de software controlar mediante programación la administración de actualizaciones. Esta interfaz proporciona funciones de administración adicionales más allá de lo que proporciona la herramienta de implementación de Office.
  
> [!NOTE]
> Este artículo se aplica a Office 2016 y versiones posteriores, Office 365. 
  
## <a name="integrating-with-the-click-to-run"></a>Integración con hacer clic y ejecutar

Para usar esta interfaz, una aplicación de administración invoca la interfaz COM y llama a las API expuestas que se comunican directamente con el servicio de instalación de hacer clic y ejecutar. 
  
> [!NOTE]
> El instalador de hacer clic y ejecutar de Office puede ejecutarse desde la línea de comandos con parámetros que pueden controlar el comportamiento, tal como se documenta en la [herramienta de implementación de Office para hacer clic y ejecutar](https://www.microsoft.com/en-us/download/details.aspx?id=49117). 
  
**A continuación se encuentra un diagrama conceptual de la interfaz COM**

![Diagrama de uso de la interfaz com en el programa de instalación de hacer clic y ejecutar de Office.] (media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "Diagrama de uso de la interfaz com en el instalador de hacer clic y ejecutar de Office")
  
El instalador de hacer clic y ejecutar de Office 365 implementa una interfaz basada en COM, **IUpdateNotify** registrada en CLSID **CLSID_UpdateNotifyObject**.
  
Esta interfaz se puede invocar de la siguiente manera:
  
```cpp
hr = CoCreateInstance(CLSID_UpdateNotifyObject, NULL, CLSCTX_ALL,
       IID_IUpdateNotify, 
      (void **)&p); 
```

La llamada solo se realizará correctamente si el autor de la llamada se ejecuta con privilegios elevados, ya que el programa de instalación de hacer clic y ejecutar debe ejecutarse con privilegios elevados.
  
La interfaz com **IUpdateNotify** expone tres funciones asincrónicas que son responsables de validar los comandos y los parámetros, y de programar la ejecución con el servicio de instalación de hacer clic y ejecutar. 
  
```cpp
HRESULT Download([in] LPWSTR pcwszParameters) // Download update content.
HRESULT Apply([in] LPWSTR pcwszParameters) // Apply update content.
HRESULT Cancel() // Cancel the download action.

```

El método, **status**, se puede usar para obtener información sobre el estado del último comando ejecutado o el estado del comando que se está ejecutando actualmente (es decir, correcto, error, códigos de error detallados).
  
```cpp
HRESULT status([out] _UPDATE_STATUS_REPORT* pUpdateStatusReport) // Get status of current action. 
typedef struct _UPDATE_STATUS_REPORT  
{  
UPDATE_STATUS status;  
UINT error; 
BSTR contentid;  
} UPDATE_STATUS_REPORT;

```

Hay cuatro Estados en los que el servicio de instalación de hacer clic y ejecutar puede encontrarse durante su ciclo de vida, durante el cual se puede llamar a los métodos de **IUpdateNotify** ; Reiniciar, inActivo, descargar y aplicar. 
  
**A continuación se encuentra el diagrama de máquina de estado de interfaz COM**

![Un diagrama de estado de la interfaz com.] (media/a409003e-6876-4ab3-bb4c-cd0c0fed5cbb.png "Un diagrama de estado para la interfaz com")
  
> [!NOTE]
> **Reiniciar**: cuando el equipo arranca, hay un período de tiempo en el que el servicio de instalación de hacer clic y ejecutar no está disponible. Una llamada correcta al método de estado después de un reinicio, devolverá eUPDATE_UNKNOWN. 
  
**Inactivo:** Cuando el programa de instalación de hacer clic y ejecutar se encuentra en estado inactivo, puede llamar a: 
  
- **Aplicar**: instalar contenido descargado anteriormente.
    
- **Cancel**: devuelve `0x800000e`"se llamó a un método en un momento inesperado".
    
- **Descargar**: descarga nuevo contenido en el cliente para su instalación posterior.
    
- **Status**: devuelve el resultado de la última acción completada o un mensaje de error si la acción finalizó por error. Si no hay ninguna acción anterior, **** status `eUPDATE_UNKNOWN`devuelve.
    
**Descargar:** Cuando el programa de instalación de hacer clic y ejecutar se encuentra en estado de descarga, puede llamar a: 
  
- **Apply**: devuelve un **HRESULT** con el valor `0x800000e`, "se llamó a un método en un momento inesperado".
    
- **Cancelar**: detiene la descarga y quita el contenido parcialmente descargado.
    
- **Download**: devuelve un **HRESULT** con el valor `0x800000e`"se llamó a un método en un momento inesperado". 
    
- **Status**: devuelve **DOWNLOAD_WIP** para indicar que el trabajo de descarga está en curso. 
    
**Aplicar:** Cuando el programa de instalación de hacer clic y ejecutar está en proceso de instalar contenido de descarga anterior: 
  
- **Apply**: devuelve un **HRESULT** con el valor `0x800000e`, "se llamó a un método en un momento inesperado".
    
- **Cancelar**: devuelve `0x800000e`, la acción Apply no se puede cancelar.
    
- **Download**: devuelve un **HRESULT** con el valor `0x800000e`"se llamó a un método en un momento inesperado". 
    
- **Status**: devuelve **APPLY_WIP** para indicar que el trabajo de aplicación está en curso. 
    
> [!NOTE]
> Dado que OfficeC2RCOM es un servicio COM+ y se carga dinámicamente, es necesario llamar a **CoCreateInstance** cada vez que se llama a un método en esta clase para garantizar que se obtiene el resultado esperado. El servicio COM+ administrará la creación de una nueva instancia si es necesario. Cuando se llama a uno de los métodos por primera vez, COM+ cargará el objeto **IUpdateNotify** y lo ejecutará dentro de una de las instancias de dllhost. exe. El nuevo objeto permanecerá activo durante unos 3 minutos de inactividad. Si se realiza una llamada subsiguiente en tres minutos después de la última llamada, el objeto **IUpdateNotify** permanecerá cargado y no se creará una nueva instancia. Si no se realiza ninguna llamada en un plazo de tres minutos, el objeto IUpdateNotify se descargará y se creará un nuevo objeto **IUpdateNotify** cuando se realice la siguiente llamada. 
  
## <a name="click-to-run-installer-com-api-reference-guide"></a>Guía de referencia de la API de COM del instalador de hacer clic y ejecutar

En la siguiente documentación de referencia de la API:
  
- Los parámetros se encuentran en un formato de par clave-valor separados por un espacio.
    
- Los parámetros no distinguen mayúsculas de minúsculas.
    
- Hay una [lista de parámetros](https://blogs.technet.microsoft.com/odsupport/2014/03/03/the-new-update-now-feature-for-office-2013-click-to-run-for-office365-and-its-associated-command-line-and-switches/) con documentación disponible. 
    
- Ahora se incluye un resumen de la interfaz de IUpdateNotify2.
    
### <a name="apply"></a>Apply

```cpp
HRESULT Apply([in] LPWSTR pcwszParameters) // Apply update content.
```

#### <a name="parameters"></a>Parameters

-  _displaylevel_: **true** para mostrar el estado de la instalación, incluidos los errores, durante el proceso de actualización; **false** para ocultar el estado de la instalación, incluidos los errores, durante el proceso de actualización. El valor predeterminado es **false**.
    
-  _forceappshutdown_: **true** para forzar que las aplicaciones de Office se cierren inmediatamente cuando se desencadena la acción **Apply** ; **false** se producirá un error si se ejecuta cualquier aplicación de Office. El valor predeterminado es **false**. Vea los [comentarios](#bk_ApplyRemark) para obtener más información. 
    
  Si se está ejecutando cualquier aplicación de Office cuando se desencadena la acción **Apply** , la acción **Apply** producirá un error. Pasar `forceappshutdown=true` al método **Apply** hará que el servicio **OfficeClickToRun** cierre inmediatamente las aplicaciones y aplique la actualización. En este caso, el usuario puede experimentar pérdida de datos. 
    
#### <a name="return-results"></a>Resultados deVueltos

|||
|:-----|:-----|
|**S_OK** <br/> |La acción se ha enviado correctamente al servicio de hacer clic y ejecutar para su ejecución.  <br/> |
|**E_ACCESSDENIED** <br/> |El autor de la llamada no se está ejecutando con privilegios elevados.  <br/> |
|**E_INVALIDARG** <br/> |Se pasaron parámetros no válidos.  <br/> |
|**E_ILLEGAL_METHOD_CALL** <br/> |La acción no está permitida en este momento. Vea los [comentarios](#bk_ApplyRemark) para obtener más información.  <br/> |

<a name="bk_ApplyRemark"></a>

#### <a name="remarks"></a>Comentarios

- Si se está ejecutando cualquier aplicación de Office cuando se desencadena la acción **Apply** , se producirá un error en la acción **Apply** . Pasar `forceappshutdown=true` al método **Apply** hará que el servicio **OfficeClickToRun** cierre inmediatamente todas las aplicaciones de Office que se estén ejecutando y aplique la actualización. El usuario puede experimentar datos porque no se le pide que guarde los cambios realizados en los documentos abiertos. 
    
- Esta acción solo se puede desencadenar cuando el estado de COM es uno de los siguientes: 
    
  - **eUPDATE_UNKNOWN**
    
  - **eDOWNLOAD_CANCELLED**
    
  - **eDOWNLOAD_FAILED**
    
  - **eDOWNLOAD_SUCCEEDED**
    
  - **eAPPLY_SUCCEEDED**
    
  - **eAPPLY_FAILED**
    
- Si se llama al método **Apply** sin descargar previamente el contenido, el método **Apply** notificará que el proceso se ha **realizado** correctamente, ya que se ha detectado que no se ha aplicado nada y que se ha completado el proceso de **aplicación** . 
    
### <a name="cancel"></a>Cancel

```cpp
HRESULT Cancel() // Cancel the download action.
```

#### <a name="return-results"></a>Resultados deVueltos

|||
|:-----|:-----|
|S_OK  <br/> |La acción se ha enviado correctamente al servicio de hacer clic y ejecutar para su ejecución.  <br/> |
|E_ILLEGAL_METHOD_CALL  <br/> |La acción no está permitida en este momento. Vea la sección [comentarios](#bk_CancelRemarks) para obtener más información  <br/> |

<a name="bk_CancelRemarks"></a>

#### <a name="remarks"></a>Comentarios

- Este método sólo se puede desencadenar cuando el identificador de estado COM **eDOWNLOAD_WIP**. Se intentará cancelar la acción de descarga actual. El estado de COM cambiará a **eDOWNLOAD_CANCELLING** y, finalmente, cambiará a **eDOWNLOAD_CANCELED**. El estado COM devolverá **E_ILLEGAL_METHOD_CALL** si se desencadena en cualquier otro momento. 
    
### <a name="download"></a>Descargar

```cpp
HRESULT Download([in] LPWSTR pcwszParameters) // Download update content.
```

#### <a name="parameters"></a>Parameters

-  _displaylevel_: **true** para mostrar el estado de la instalación, incluidos los errores, durante el proceso de actualización; **false** para ocultar el estado de la instalación, incluidos los errores, durante el proceso de actualización. El valor predeterminado es **false**.
    
-  _updatebaseurl_: dirección URL al origen de descarga alternativo.
    
-  _updatetoversion_: versión en la que se va a actualizar Office. Defina este parámetro si desea actualizar a una versión anterior a la versión instalada actualmente.
    
-  _downloadsource_: CLSID de la implementación de **IBackgroundCopyManager** personalizada (Administrador de bits). 
    
-  _contentid_: identifica el contenido que se va a descargar desde el servidor de contenido mediante el administrador de bits personalizado. Este valor se pasa a través de la interfaz de BITS para la interpretación.
    
#### <a name="return-results"></a>Resultados deVueltos

|||
|:-----|:-----|
|**S_OK** <br/> |La acción se ha enviado correctamente al servicio de hacer clic y ejecutar para su ejecución.  <br/> |
|**E_ACCESSDENIED** <br/> |El autor de la llamada no se está ejecutando con privilegios elevados.  <br/> |
|**E_INVALIDARG** <br/> |Se pasaron parámetros no válidos.  <br/> |
|**E_ILLEGAL_METHOD_CALL** <br/> |La acción no está permitida en este momento. Vea los [comentarios](#bk_DownloadRemark) para obtener más información.  <br/> |

<a name="bk_DownloadRemark"></a>

#### <a name="remarks"></a>Comentarios

- Debe especificar _downloadsource_ y _contentid_ como un par. De lo contrario, el método **download** devolverá un error **E_INVALIDARG** . 
    
- Si se proporciona _downloadsource_, _contentid_y _updatebaseurl_ , se omitirá _updatebaseurl_ . 
    
- Esta acción solo se puede desencadenar cuando el estado de COM es uno de los siguientes: 
    
  - **eUPDATE_UNKNOWN**
    
  - **eDOWNLOAD_CANCELLED**
    
  - **eDOWNLOAD_FAILED**
    
  - **eDOWNLOAD_SUCCEEDED**
    
  - **eAPPLY_SUCCEEDED**
    
  - **eAPPLY_FAILED**
    
- Si se llama al método **Apply** sin descargar previamente el contenido, el método **Apply** informará de que el proceso se ha detectado correctamente, ya que se ha detectado que no se ha aplicado nada y se ha completado el proceso de **aplicación** . **** 
    
#### <a name="examples"></a>Ejemplos

- Para descargar el contenido del administrador de BITS personalizado: llame a la función **download ()** y pase los siguientes parámetros: 
    
  ```cpp
  "downloadsource=CLSIDofBITSInterface contentid=BITSServerContentIdentifier"
  ```

- Para descargar el contenido de la red CDN de Microsoft: llame a la función **download ()** sin especificar los parámetros _downloadsource_, _contentid_o _updatebaseurl_ . 
    
- Para descargar el contenido desde una ubicación personalizada: llame a la función **download ()** y pase el parámetro siguiente: 
    
  ```cpp
  "updatebaseurl=yourcontentserverurl"
  ```

### <a name="status"></a>Estado

```cpp
typdef struct _UPDATE_STATUS_REPORT
{
    UPDATE_STATUS status;
    UINT error;
    LPCWSTR contentid;
}UPDATE_STATUS_REPORT;
HRESULT status([out] _UPDATE_STATUS_REPORT& pUpdateStatusReport) // Get status of current action
```

#### <a name="parameters"></a>Parameters

|||
|:-----|:-----|
| _pUpdateStatusReport_ <br/> |Puntero a una estructura UPDATE_STATUS_REPORT.  <br/> |
   
#### <a name="return-results"></a>Resultados deVueltos

|||
|:-----|:-----|
|**S_OK** <br/> |El **** método status siempre devuelve este resultado. Inspeccione `UPDATE_STATUS_RESULT` la estructura del estado de la acción actual.  <br/> |
   
#### <a name="remarks"></a>Comentarios

- El campo Estado de `UPDATE_STATUS_REPORT` contiene el estado de la acción actual. Se devuelve uno de los siguientes valores de estado: 
    
  ```cpp
  typedef enum _UPDATE_STATUS
  {
  eUPDATE_UNKNOWN = 0,
  eDOWNLOAD_PENDING,
  eDOWNLOAD_WIP,
  eDOWNLOAD_CANCELLING,
  eDOWNLOAD_CANCELLED,
  eDOWNLOAD_FAILED,
  eDOWNLOAD_SUCCEEDED,
  eAPPLY_PENDING,
  eAPPLY_WIP,
  eAPPLY_SUCCEEDED,
  eAPPLY_FAILED,
  } UPDATE_STATUS;
  
  ```

- Si se produce un error en el último comando, el campo de error `UPDATE_STATUS_REPORT` del contiene información detallada sobre el error. Se devuelven dos tipos de códigos de **** error del método status. 
    
- Si el error es menor `UPDATE_ERROR_CODE::eUNKNOWN`que, el error es uno de los siguientes códigos de error predefinidos:
    
  ```cpp
  typedef enum _UPDATE_ERROR_CODE
  {
  eOK = 0,
  eFAILED_UNEXPECTED,
  eTRIGGER_DISABLED,
  ePIPELINE_IN_USE,
  eFAILED_STOP_C2RSERVICE,
  eFAILED_GET_CLIENTUPDATEFOLDER,
  eFAILED_LOCK_PACKAGE_TO_UPDATE,
  eFAILED_CREATE_STREAM_SESSION,
  eFAILED_PUBLISH_WORKING_CONFIGURATION,
  eFAILED_DOWNLOAD_UPGRADE_PACKAGE,
  eFAILED_APPLY_UPGRADE_PACKAGE,
  eFAILED_INITIALIZE_RSOD,
  eFAILED_PUBLISH_RSOD,
  // Keep this one as the last
  eUNKNOWN
  } UPDATE_ERROR_CODE;
  
  ```

  Si el código de error devuelto es `UPDATE_ERROR_CODE::eUNKNOWN` mayor que el **valor HRESULT** de una llamada a una función fallida. Para extraer el valor de `UPDATE_ERROR_CODE::eUNKNOWN` resta de HRESULT del valor devuelto en el campo `UPDATE_STATUS_REPORT`de error del.
    
  Para ver la lista completa de valores de estado y error, inspeccione la biblioteca de tipos de **IUpdateNotify** incrustada en OfficeC2RCom. dll. 
    
- El campo contentid se usa para las llamadas al **Estado** una vez iniciaDa la **descarga** y devuelve el elemento contentid que se pasó a la llamada a **download** . Se recomienda inicializar este campo en **null** antes de llamar al método status **** y, a continuación, comprobar el valor una vez que se ha devuelto el **Estado** . Si el valor todavía es **null**, significa que no hay contentid para devolver. Si el valor no es **null**, debe liberarlo con una llamada a **SysFreeString ()**. A continuación, se muestra un fragmento de código sobre cómo llamar al **Estado** después de la **descarga**.
    
  ```cpp
  std::wstring contentID;
  UPDATE_STATUS_REPORT statusReport;
  statusReport.status = eUPDATE_UNKNOWN;
  statusReport.error = eOK;
  statusReport.contentid = NULL;
  hr = p->Status(&statusReport);
  if (statusReport.contentid != NULL)
  {
  contentID = statusReport.contentid;
  SysFreeString(statusReport.contentid);
  }
  wprintf(L"ContentID: %s, Status: %d, LastError: %d", contentID.c_str(), statusReport.status, statusReport.error);
  
  ```

### <a name="summary-of-iupdatenotify2-interface"></a>Resumen de la interfaz de IUpdateNotify2

> [!NOTE]
> Este resumen se proporciona como una información de complementos para [la integración de aplicaciones de administración con el instalador de hacer clic y ejecutar de Office 365](https://msdn.microsoft.com/EN-US/library/office/mt608768.aspx). Una vez que se actualiza el documento público, este documento puede considerarse obsoleto. 
  
De C2RTenant [16.0.8208.6352](https://oloop/BuildGroup/Details/tenantc2rclient#3519/1255278) (la primera compilación disponible públicamente debe ser la compilación de la horquilla de junio--8326. *) se ha agregado una nueva interfaz de **IUpdateNotify2** . A continuación se muestra información básica sobre esta interfaz: 
  
- CLSID_UpdateNotifyObject2, {52C2F9C2-F1AC-4021-BF50-756A5FA8DDFE}
    
- Esta interfaz también hospedaba la interfaz IUpdateNotify original para proporcionar compatibilidad con versiones anteriores. Lo que significa que si usa esta interfaz, tiene acceso a todos los métodos proporcionados en la interfaz **UpdateNotifyObject** . 
    
- Nuevos métodos agregados a IUpdateNotify2:
    
  - **HRESULT** GetBlockingApps ([salida] BSTR \* AppsList). Obtener actualizaciones bloqueo de la lista de aplicaciones. Esta llamada devolverá la ejecución de aplicaciones de Office que impedirán que el proceso de actualización continúe. 
    
  - **HRESULT** GetOfficeDeploymentData ([in] int DataType, [in] **LPCWSTR** pcwszName, [out] BSTR * OfficeData). Obtener datos de implementación de Office. 
    
- Si desea usar los nuevos métodos, debe asegurarse de lo siguiente:
    
  - La versión de C2R es más reciente que la compilación\>anterior (= compilación de la bifurcación de junio).
    
  - Use UpdateNotifyObject2, en lugar de **UpdateNotifyObject** para llamar a **CoCreateInstance**.
    
Si no usa ninguno de los métodos nuevos, no es necesario cambiar nada. Todos los métodos existentes funcionarán exactamente del mismo modo que antes.
  
## <a name="implementing-the-bits-interface"></a>Implementación de la interfaz de BITS

El [servicio de transferencia inteligente en segundo plano](https://msdn.microsoft.com/library/bb968799(v=vs.85).aspx) (bits) es un servicio proporcionado por Microsoft para transferir archivos entre un cliente y un servidor. BITS es uno de los canales que puede usar el instalador de hacer clic y ejecutar de Office para descargar contenido. De forma predeterminada, el instalador de hacer clic y ejecutar de Office usa la implementación de BITS de Windows integrada para descargar el contenido de la red CDN. 
  
Al suministrar una implementación BITS personalizada al método **download ()** de la interfaz **IUpdateNotify** , el software de administración puede controlar dónde y cómo descarga el contenido el cliente. Una interfaz de BITS personalizada es útil cuando se proporciona un canal de distribución de contenido personalizado distinto de los canales integrados de hacer clic y ejecutar, como la red CDN de Office, los servidores IIS o los recursos compartidos de archivos. 
  
El requisito mínimo para que una interfaz de BITS personalizada funcione con Office C2R Service es:
  
- Para **IBackgroundCopyManager**:
    
  ```cpp
  HRESULT _stdcall CreateJob(
                      [in] LPWSTR DisplayName, 
                      [in] BG_JOB_TYPE Type, 
                      [out] GUID* pJobId, 
                      [out] IBackgroundCopyJob** ppJob)
  HRESULT _stdcall GetJob(
                      [in] GUID* jobID, 
                      [out] IBackgroundCopyJob** ppJob)
  HRESULT _stdcall EnumJobs(
                      [in] unsigned long dwFlags, 
                      [out] IEnumBackgroundCopyJobs** ppenum)
  
  ```

- Para **IBackgroundCopyJob**:
    
  ```cpp
  HRESULT _stdcall AddFile(
                      [in] LPWSTR RemoteUrl, 
                      [in] LPWSTR LocalName)
  HRESULT _stdcall Resume()
  HRESULT _stdcall Complete()
  HRESULT _stdcall Cancel();
  HRESULT _stdcall GetState([out] BG_JOB_STATE* pVal);
  HRESULT GetProgress( [out] BG_JOB_PROGRESS *pProgress);
  
  ```

- Para **IBackgroundCopyJob3**:
    
  ```cpp
  HRESULT _stdcall AddFileWithRanges(
                      [in] LPWSTR RemoteUrl, 
                      [in] LPWSTR LocalName,
                      [in] DWORD RangeCount,
                      [in] BG_FILE_RANGE Ranges[])
  
  ```

- Para las `Addfile` funciones `AddFileWithRanges` y, la dirección URL remota tiene el siguiente formato: 
    
  ```cpp
  cmbits://<contentid>/<relative path to target file>
  ```

  - cmbits está codificado de forma rígida y representa BITS personalizados.
    
  -  __ **** _\> contentid es el parámetro contentid del método \<_ download (). 
    
  -  _ruta de acceso relativa al\> archivo de destino proporciona la ubicación y el nombre del archivo que se va a descargar. \<_ 
    
    Por ejemplo, si ha proporcionado un _contentid_ del al `f732af58-5d86-4299-abe9-7595c35136ef` método **download ()** y Office C2R desea descargar el archivo CAB de la versión, `v32.cab` como File, llamará a **AddFile ()** con lo siguiente `RemoteUrl`:
    
  ```cpp
  cmbits://f732af58-5d86-4299-abe9-7595c35136ef/Office/Data/V32.cab
  ```

- Para **IBackgroundCopyError**:
    
  ```cpp
  HRESULT _stdcall GetErrorDescription(
        [in]  DWORD  LanguageId,
        [out] LPWSTR *ppErrorDescription);
  
  ```

- Para **IBackgroundCopyFile**:
    
  ```cpp
  HRESULT _stdcall GetLocalName([out] LPWSTR *ppName); 
  HRESULT _stdcall GetRemoteName([out] LPWSTR *ppName);
  
  ```

<!--## Automating content staging

IT administrators can choose to have desktop clients enabled to automatically receive updates when they are available directly from the Microsoft Content Delivery Network (CDN) or they can choose to control the deployment of updates available from the [update channels](https://support.office.com/en-us/article/Overview-of-update-channels-for-Office-365-ProPlus-9ccf0f13-28ff-4975-9bd2-7e4ea2fefef4?ui=en-US&rs=en-US&ad=US) using the [Office 2016 Deployment Tool](https://www.microsoft.com/en-us/download/details.aspx?id=49117) or [System Center Configuration Manager](https://support.office.com/en-us/article/Manage-updates-to-Office-365-ProPlus-with-System-Center-Configuration-Manager-b4a17328-fcfe-40bf-9202-58d7cbf1cede).
  
The service supports the ability for management tools to recognize and automate the download of the content when updates are made available.
  
**Following is a diagram showing the overview of downloading a custom image**

![An overview of downloading Office updates from the CDN.](media/9afac230-6b22-4526-a800-0562708cc436.png "An overview of downloading Office updates from the CDN")
  
In the above diagram you see that a new Office 365 ProPlus image is available on the Office Content Distribution Network (CDN). Along with the Office 365 ProPlus image, an XML-formatted file list is also available which has the information needed to enable manageability software to directly create customized images replacing the need for using the Office Deployment Tool.
  
An enterprise configures their WSUS to sync the Office 365 Client Updates. These updates do not contain the actual image payload but does allow the manageability software to recognize when new content is available. The manageability software can then read the Client Update metadata to understand what version of Office the update applies to.
  
If the update is applicable, the manageability software can use the CDN content and the file list to create the custom image and store it onto the file share location that it is configured to use.
  
### Format of the XML file list

There are two file lists available in a cab file on the CDN. One lists the files for the 32-bit version of Office and one for the 64-bit version of Office. The URL of the location of the Office File List (OFL.CAB) file is [https://officecdn.microsoft.com/pr/wsus/ofl.cab](https://officecdn.microsoft.com/pr/wsus/ofl.cab). The two file lists are called:
  
- O365Client_32bit.xml
    
- O365Client_64bit.xml
    
Within the XML for each of the file lists is an  `UpdateFiles` node which contains a version attribute.  `UpdateFiles version="1.4"`.
  
This version is incremented if changes are made to the file lists.
  
There are two parameters that need to be combined with the XML to make a custom image: 
  
- Replace  _%version%_ with the build version of Office. This can be derived from the Client Update metadata  `MoreInfoURL` field, see below. 
    
- Define  _baseURL_ by using the URL value associated with the branch the image is being created for. This can be derived from the Client Update metadata, see below. 
    
The steps for creating an image are:
  
1. Open the XML file list.
    
2. Replace occurrences of  _%version%_ with the applicable Office build version. The build version can be acquired from releasehistory.xml as described later in this article. 
    
3. Read the URL attribute for the target branch.
    
4. Remove language nodes for any languages not required in the custom image.
    
   > [!NOTE]
   > Nodes with language='0' are language neutral and must be included in the image. 
  
5. Construct a local image of the CDN by iterating through the XML file list and copying the CDN files, while creating the folder structure as needed. 
    
   - If the  _rename_ attribute is provided, then rename the copied file to the value provided in the  _rename_ attribute. This used to create the top-level default v64.cab and v32.cab files. These are the renamed versions of the top-level build cab file and are used as the default installation version if the version is not specified. 
    
   - Use URL + relativePath + filename to construct the CDN location.
    
The following examples use the Monthly channel (as defined by the  `baseURL` node) and build version 16.0.4229.1004 from releasehistory.xml. 
  
```cpp
baseURL branch="Monthly" URL="https://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60" /
```

- The following is a language neutral file needed for all languages. The name of the file is v64_16.0.4229.1004.cab and it should be copied from https://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/v64_16.0.4229.1004.cab and renamed to …/office/data/v64.cab.
    
  ```cpp
  baseURL branch="Business" URL="https://officecdn.microsoft.com/pr/7ffbc6bf-bc32-4f92-8982-f9dd17fd3114" /
  File name="v64_%version%.cab" rename="v64.cab" relativePath="/office/data/" language="0"/
  
  ```

- The following is a file to be included in the en-US image as designated by the language LCID=1033. The name of the file is s641033.cab and it should be copied from https://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/16.0.4229.1004/s641033.cab and not renamed.
    
  ```cpp
  File name="s641033.cab" relativePath="/office/data/%version%/" language="1033" /
  ```

### Hash verification of data files

Image creation tools may verify the integrity of the downloaded .dat files by comparing a computed HASH value with the supplied HASH value associated with each of the .dat files. Below is an example of a .dat file from the Monthly channel with build version 16.0.4229.1004 and language set to Bulgarian.
  
```cpp
File name="stream.x64.bg-bg.dat" hashLocation="s641026.cab/stream.x64.bg-bg.hash" hashAlgo="Sha256" relativePath="/office/data/%version%/" language="1026"
```

- The  _hashLocation_ attribute specifies the relative path location of the stream.x64.bg-bg.hash for the stream.x64.bg-bg.dat file. Construct the hash file location by concatenating URL + relativePath + hashLocation. In this example the stream.x64.bg-bg.hash location would be https://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/16.0.4229.1004/s641026.cab/stream.x64.bg-bg.hash 
    
- The  _hashAlgo_ attribute specifies what hashing algorithm was used. In this case the Sha256 algorithm was used. 
    
To validate the integrity of the stream.x64.bg-bg.dat file, open the stream.x64.bg-bg.hash and read the hash value from the first line of text in the hash file. Compare this to the has value that you computed using the specified hashing algorithm to verify that the values match. Use the following C# code to read the hash.
  
```cs
string[] readHashes = System.IO.File.ReadAllLines(tmpFile, Encoding.Unicode);
string readHash = readHashes.First();

```

### Office 365 Client Updates

Office 365 Client Updates enable manageability software to treat the Office 365 Client Updates in a manner very similar to any other WU update with one exception; the client updates do not contain an actual payload. The Office 365 Client Updates should not be installed on any clients but rather used to trigger the workflows with the manageability software replacing the installation command with the COM based installation mechanism shown above.
  
**Office 365 Client Update workflow**

![Workflow diagram for O365PP client updates.](media/bc8092b0-62b8-402c-a5c0-04d55cca01d4.png "Workflow diagram for O365PP client updates")
  
Each Office 365 Client Update that is published includes metadata about the update. This metadata includes a parameter called  _MoreInfoUrl_ which can be used to derive the following information: 
  
-  _Ver_: Identifies the Office version associated with this update. For example 16.0.4229.1004.
    
-  _Branch_: Identifies the Update Channel for this update. Values include InsiderFast, Insiders, Monthly, Targeted, Broad. Additional values may be added in the future.
    
-  _Arch_: Identifies the processor architecture associated with this update.
    
-  _xmlVer_: Identifies the version of the XML file lists to use to construct the base image for this update.
    
-  _xmlPath_: Path to the OFL.CAB file that contains the XML file lists.
    
-  _xmlFile_: The name of the file list that should be used for this update. The value will be  `O365Client_32bit` or  `O365Client_64bit` and will match the value in  _Arch_.
    
The following is an example of the  _MoreInfoURL_ parameter which refers to the Office 365 Client Update for the 32-bit version of Office with build version of 16.0.2342.2343 on the Current channel. 
  
```http
https://officecdn.microsoft.com/pr/wsus/ofl.cab is the location of the XML file lists for this update, specifically the O365Client_32bit.xml from within the OFL.CAB.
https://go.microsoft.com/fwlink/?LinkId=626090&Ver=16.0.8326.2096&Branch=Current&Arch=64&XMLVer=1.4&xmlPath=https://officecdn.microsoft.com/pr/wsus/ofl.cab&xmlFile=O365Client_64bit.xml 

```
THE ABOVE SECTION APPEARS TO BE A DUPLICATE OF THE FOLLOWING SECTION; TEMPORARILY COMMENTING IT OUT.-->

## <a name="automating-content-staging"></a>Automatizar el almacenamiento provisional del contenido

Los administradores de TI pueden elegir que los clientes de escritorio reciban automáticamente actualizaciones cuando están disponibles directamente desde la red de entrega de contenido (CDN) de Microsoft o pueden elegir controlar la implementación de las actualizaciones disponibles en la actualización. canales con la herramienta de implementación de Office o System Center Configuration Manager.
  
El servicio admite la capacidad de las herramientas de administración para reconocer y automatizar la descarga del contenido cuando las actualizaciones estén disponibles.
  
**La siguiente imagen es una introducción a la descarga de una imagen personalizada**

![Diagrama de uso de la interfaz com en el programa de instalación de hacer clic y ejecutar de Office.] (media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "Diagrama de uso de la interfaz com en el instalador de hacer clic y ejecutar de Office")
  
### <a name="overview-of-downloading-a-custom-image"></a>Información general sobre la descarga de una imagen personalizada
  
En el diagrama anterior, verá que una imagen nueva de Office 365 proPlus está disponible en la red de distribución de contenido (CDN) de Office. Junto con la imagen de Office 365 proPlus, también hay disponible una lista de archivos con formato XML que contiene la información necesaria para que el software de administración pueda crear imágenes personalizadas directamente, lo que reemplaza la necesidad de usar la herramienta de implementación de Office.
  
Una empresa configura su WSUS para que sincronice las actualizaciones de cliente de Office 365. Estas actualizaciones no contienen la carga real de la imagen, pero sí permiten que el software de administración reconozca cuando hay contenido nuevo disponible. El software de administración puede leer los metadatos de actualización del cliente para comprender a qué versión de Office se aplica la actualización.
  
Si la actualización es aplicable, el software de administración puede usar el contenido de la red CDN y la lista de archivos para crear la imagen personalizada y almacenarla en la ubicación del recurso compartido de archivos que está configurada para usar.
  
### <a name="format-of-the-xml-file-list"></a>Formato de la lista de archivos XML

Hay dos listas de archivos disponibles en un archivo CAB en la red CDN. Uno enumera los archivos de la versión de 32 bits de Office y otro para la versión de 64 bits de Office. La dirección URL de la ubicación de la lista de archivos de Office (OFL. CAB) es [https://officecdn.microsoft.com/pr/wsus/ofl.cab](https://officecdn.microsoft.com/pr/wsus/ofl.cab). Se llama a las dos listas de archivos:
  
- O365Client_32bit. XML
    
- O365Client_64bit. XML
    
Dentro del código XML para cada una de las listas de <UpdateFiles> archivos se encuentra un nodo que contiene un atributo version.  `<UpdateFiles version="1.4">`. Esta versión se incrementa si se realizan cambios en las listas de archivos.
  
Hay dos parámetros que deben combinarse con el XML para crear una imagen personalizada: 
  
- Reemplace *% versión%* por la versión de compilación de Office. Esto puede derivarse de los metadatos de actualización de cliente (que se explican en la sección siguiente). 
    
- Defina *baseurl* mediante el valor de dirección URL asociado a la rama para la que se está creando la imagen. Esto se deriva de los metadatos de actualización del cliente, que se explican en la siguiente sección. 
    
Los pasos para crear una imagen son los siguientes:
  
1. Abra la lista de archivos XML.
    
2. Reemplace las repeticiones de *% version%* por la versión de compilación de Office aplicable. La versión de compilación puede adquirirse de releasehistory. XML, como se describe más adelante en este artículo. 
    
3. Lea el atributo de dirección URL de la rama de destino.
    
4. Quita los nodos de idioma de los idiomas que no se necesitan en la imagen personalizada.
    
   > [!NOTE]
   > Los nodos con Language = ' 0 ' son independientes del idioma y deben incluirse en la imagen. 
  
5. Construya una imagen local de la red CDN iterando por la lista de archivos XML y copiando los archivos de la red CDN, a la vez que crea la estructura de carpetas según sea necesario. 
    
   - Si se proporciona el atributo *Rename* , cambie el *nombre* del archivo copiado al valor proporcionado en el atributo Rename. Se usa para crear los archivos V64. cab y V32. cab predeterminados de nivel superior. Estas son las versiones a las que se ha cambiado el nombre del archivo CAB de compilación de nivel superior y se usan como la versión de instalación predeterminada si no se especifica la versión. 
    
   - Use URL + relativePath + FILENAME para construir la ubicación de la red CDN.
    
Los siguientes son ejemplos que usan el canal mensual (definido por el `<baseURL>` nodo) y la versión de compilación 16.0.4229.1004 desde releasehistory. Xml. 
  
```xml
<baseURL branch="Monthly" URL="https://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60" />
```

- A continuación se encuentra un archivo independiente del idioma necesario para todos los idiomas. El nombre del archivo es v64_ 16.0.4229.1004. cab y debe copiarse `https://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/v64_16.0.4229.1004.cab` y cambiar su nombre a. `…/office/data/v64.cab` 
    
  ```xml
  <File name="v64_%version%.cab" rename="v64.cab" relativePath="/office/data/" language="0"/>
  
  ```

- A continuación se incluye un archivo que se incluirá en la imagen en-US, tal como lo designe el LCID del idioma = 1033. El nombre del archivo es s641033. cab y debe copiarse y no cambiarse de `https://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/16.0.4229.1004/s641033.cab` nombre.
    
  ```xml
  <File name="s641033.cab" relativePath="/office/data/%version%/" language="1033" />
  ```

### <a name="hash-verification-of-dat-files"></a>Comprobación de hash de los archivos. dat

Las herramientas de creación de imágenes pueden comprobar la integridad de los archivos. dat descargados mediante la comparación de un valor HASH calculado con el valor HASH proporcionado asociado con cada uno de los archivos. dat. A continuación se proporciona un ejemplo de un archivo. dat desde el canal mensual con la versión de compilación 16.0.4229.1004 y el idioma configurado en búlgaro:
  
```xml
<File name="stream.x64.bg-bg.dat" hashLocation="s641026.cab/stream.x64.bg-bg.hash" hashAlgo="Sha256" relativePath="/office/data/%version%/" language="1026"/>
```

- El atributo **hashLocation** especifica la ubicación de la ruta de acceso relativa del Stream.x64.BG-BG. hash para el archivo Stream.x64.BG-BG. dat. Construya la ubicación del archivo hash concatenando la dirección URL + relativePath + hashLocation. En el siguiente ejemplo, la ubicación de stream.x64.bg-BG. hash sería: 
    
  ```http
  https://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/16.0.4229.1004/s641026.cab/stream.x64.bg-bg.hash 
  ```

- El atributo **hashAlgo** especifica el algoritmo hash que se usó. En este caso, se utilizó Sha256. 
    
  Para validar la integridad del archivo stream.x64.bg-BG. dat, abra el stream.x64.bg-BG. hash y lea el valor de HASH, que es la primera línea de texto del archivo hash. Compare esto con el valor hash calculado (con el algoritmo hash especificado) para comprobar la integridad del archivo. dat descargado.
    
  En el ejemplo siguiente se muestra el código de C# para leer el hash.
    
  ```cs
    string[] readHashes = System.IO.File.ReadAllLines(tmpFile, Encoding.Unicode);
    string readHash = readHashes.First();
  ```

### <a name="office-365-client-updates"></a>Actualizaciones de cliente de Office 365

Todas las actualizaciones de cliente de Office 365 se publican en el [Catálogo de Microsoft Update](https://www.catalog.update.microsoft.com/Search.aspx?q=office+365+client).
  
Las actualizaciones de cliente de Office 365 permiten que el software de administración trate las actualizaciones de cliente de Office 365 de forma muy similar a cualquier otra actualización de WU con una excepción; las actualizaciones de cliente no contienen una carga real. Las actualizaciones de cliente de Office 365 no deben instalarse en ningún cliente, sino que se usan para desencadenar flujos de trabajo con el software de administración que reemplaza el comando de instalación por el mecanismo de instalación basado en COM mostrado anteriormente. 
  
**En la siguiente figura se muestra un diagrama del flujo de trabajo de actualización de cliente de Office 365.**

![Diagrama de flujo de trabajo para las actualizaciones de cliente de O365PP.] (media/bc8092b0-62b8-402c-a5c0-04d55cca01d4.png "Diagrama de flujo de trabajo para actualizaciones de cliente de O365PP")
  
Cada actualización de cliente de Office 365 que está publicada incluye metadatos sobre la actualización. Estos metadatos incluyen un parámetro denominado *MoreInfoUrl* que se puede usar para derivar la siguiente información: 
  
-  *Ver*: identifica la versión de Office asociada a esta actualización. 
    
-  *Branch*: identifica el canal de actualización para esta actualización. Los valores incluyen InsiderFast, Insider, mensual, dirigido, general. Es posible que se agreguen valores adicionales en el futuro. 
    
-  *Arch*: identifica la arquitectura del procesador asociada con esta actualización. 
    
-  *xmlVer*: la versión de las listas de archivos XML que se deben usar para construir la imagen base para esta actualización. 
    
-  *xmlPath*: ruta de acceso al OFL. Archivo CAB que contiene las listas de archivos XML. 
    
-  *mlFile*: nombre de la lista de archivos que se debe usar para esta actualización. El valor será O365Client_32bit o O365Client_64bit, y coincidirá con el arco. 
    
La siguiente dirección URL es un ejemplo del parámetro *MoreInfoURL* que hace referencia a las versiones de actualización de cliente de Office 365 para la versión de 32 bits de Office con la versión de compilación de 16.0.2342.2343 en el canal actual. 
  
https://officecdn.microsoft.com/pr/wsus/ofl.cabes la ubicación de las listas de archivos XML para esta actualización, en concreto O365Client_32bit. XML desde el OFL. Gabinete.
  
[Versiones de canal de actualización de cliente de Office 365](https://go.microsoft.com/fwlink/?LinkId=626090&Ver=16.0.8326.2096&Branch=Current&Arch=64&XMLVer=1.4&xmlPath=https://officecdn.microsoft.com/pr/wsus/ofl.cab&xmlFile=O365Client_64bit.xml)
  
### <a name="additional-metadata-for-automating-content-staging"></a>Metadatos adicionales para automatizar el contenido provisional

Además de los metadatos publicados que definen, hay también archivos XML adicionales publicados en la red CDN que pueden ayudar a proporcionar información adicional sobre los clientes de Office 365 que están disponibles en la red CDN de Office.
  
**SKU. XML**
  
Este archivo XML está contenido en un archivo CAB firmado y se publica en la red CDN de Office en [https://officecdn.microsoft.com/pr/wsus/skus.cab](https://officecdn.microsoft.com/pr/wsus/skus.cab)la siguiente dirección URL:.
  
Los metadatos publicados en este archivo XML son útiles para determinar qué productos están disponibles para la implementación y el servicio desde la red CDN de Office junto con varias opciones para cada uno. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<ReleaseInfo PublishedDate="08/07/2017 16:34">
  <!-- Suite / App catalog -->
  <Suite>
    <SKU Name="Office 365 ProPlus" ProductID="O365ProPlusRetail" Default="True">
      <Apps>
        <App Name="Access" AppID="Access" />
        <App Name="Excel" AppID="Excel" />
        <App Name="OneDrive for Business (Groove)" AppID="Groove" />
        <App Name="OneDrive for Business (Next Gen Sync Client)" AppID="OneDrive" />
        <App Name="OneNote" AppID="OneNote" />
        <App Name="Outlook" AppID="Outlook" />
        <App Name="PowerPoint" AppID="PowerPoint" />
        <App Name="Publisher" AppID="Publisher" />
        <App Name="Skype for Business" AppID="Lync" />
        <App Name="Word" AppID="Word" />
      </Apps>
      <Channels>
        <Channel ID="Monthly"/>
        <Channel ID="Insiders"/>
        <Channel ID="Targeted"/>
        <Channel ID="Broad"/>
      </Channels>
    </SKU>
```

ReleaseInfo nodo raíz contiene el atributo PublishedDate que identifica la fecha en que se publicó este archivo. ** \<\> ** 
  
El nodo **SKU\> identifica una SKU individual. \<** 
  
- El atributo *ProductID* identifica el identificador que se pasa como el atributo ID en Configuration. xml si se usa la ODT. Por ejemplo, `<Product ID="O365ProPlusRetail">`. 
    
- El atributo *default* , si se establece en true, identifica el SKU recomendado. 
    
Los nodos de la **aplicación\> se usan para definir las aplicaciones de Office individuales que admite cada SKU. \<** 
  
- El atributo *Name* es el nombre de la aplicación que se muestra. 
    
- El atributo *AppID* es el atributo ID que se pasa en Configuration. XML para ** \<el\> nodo ExcludeApp** si se usa la ODT. Por ejemplo, `<ExcludeApp ID="Publisher" />`. 
    
**RELEASEHISTORY. XML**
  
Este archivo XML está contenido en un archivo CAB firmado y se publica en la red CDN de Office en [https://officecdn.microsoft.com/pr/wsus/releasehistory.cab](https://officecdn.microsoft.com/pr/wsus/releasehistory.cab)la siguiente ubicación:. 
  
Los metadatos publicados en este archivo XML son útiles para determinar qué canales se admiten para el servicio de actualizaciones desde la red CDN de Office junto con información sobre el historial de la compilación para cada uno de los canales admitidos.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<ReleaseHistory PublishedDate="10/22/2017 00:48">
  <UpdateChannel Name="Current" ID="Monthly" DisplayName="Monthly Channel">
    <Update Latest="True" Version="1709" LegacyVersion="16.0.8528.2139" Build="8528.2139" PubTime="2017-10-16T19:45:50.743Z" />
    <Update Latest="False" Version="1708" LegacyVersion="16.0.8431.2107" Build="8431.2107" PubTime="2017-10-11T01:52:33.793Z" />
    <Update Latest="False" Version="1708" LegacyVersion="16.0.8431.2079" Build="8431.2079" PubTime="2017-09-18T22:26:13.673Z" />
    <Update Latest="False" Version="1707" LegacyVersion="16.0.8326.2107" Build="8326.2107" PubTime="2017-09-12T18:56:53.657Z" />
    <Update Latest="False" Version="1707" LegacyVersion="16.0.8326.2096" Build="8326.2096" PubTime="2017-08-30T00:10:25.253Z" />
    <Update Latest="False" Version="1707" LegacyVersion="16.0.8326.2076" Build="8326.2076" PubTime="2017-08-19T00:13:01.787Z" />
    <Update Latest="False" Version="1707" LegacyVersion="16.0.8326.2073" Build="8326.2073" PubTime="2017-08-11T19:35:42.173Z" />
  </UpdateChannel>
```

El nodo raíz ** \<ReleaseHistory\> ** contiene el atributo PublishedDate, que identifica la fecha en que se publicó el archivo. 
  
El ** \<nodo\> UpdateChannel** define un canal admitido. 
  
- El atributo *Name* define el identificador de canal que se usa para pasar a la ODT en Configuration. XML como el atributo de canal. 
    
  Ejemplo: `<Add SourcePath="\\Server\Share" OfficeClientEdition="32" Channel="Current">` 
    
  > [!NOTE] 
  > Este atributo se ha dejado de usar y solo se usa para compatibilidad con versiones anteriores. Use el atributo ID en vez del atributo name. 
    
- El atributo *ID* define el identificador de canal que se usa para pasar a la ODT en Configuration. XML como el atributo de canal. 
    
  Ejemplo: `<Add SourcePath="\\Server\Share" OfficeClientEdition="32" Channel="Deferred">` 
    
- El atributo **displayName** se usa como el nombre para mostrar. 
    
El ** \<nodo\> actualizar** se usa para definir cada actualización que se ha publicado para ese canal en particular. 
  
- El atributo **último** , si se establece en true, define la versión más reciente de ese canal. 
    
- El atributo **version** define el número de versión para esta actualización en particular. 
    
- El atributo **LegacyVersion** define el número de versión completo de esta actualización en particular. 
    
- El atributo **Build** define el número de compilación de esta actualización en particular. 
    
- El atributo **PubTime** define la fecha y la hora en la que se publicó la actualización en la red CDN de Office. 
    

