---
title: Integración de aplicaciones de la capacidad de administración con el instalador de click-to-run de Office 365
manager: kelbow
ms.date: 10/22/2017
ms.audience: ITPro
localization_priority: Normal
ms.assetid: c0fa8fed-1585-4566-a9be-ef6d6d1b4ce8
description: Obtenga información sobre cómo integrar al instalador de Office 365 Click-to-Run con una solución de administración de software.
ms.openlocfilehash: cdcdde0618e2b96ce997ba5e263f75d85c21fd11
ms.sourcegitcommit: 4590b7ed906d008693a58abe63f089ed8a380b34
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/21/2018
ms.locfileid: "26643223"
---
# <a name="integrating-manageability-applications-with-office-365-click-to-run-installer"></a>Integración de aplicaciones de la capacidad de administración con el instalador de click-to-run de Office 365

Obtenga información sobre cómo integrar al instalador de Office 365 Click-to-Run con una solución de administración de software.
  
El instalador de Office 365 Click-to-Run proporciona una interfaz COM que permite a los profesionales de TI y soluciones de administración de software control mediante programación a través de la administración de actualizaciones. Esta interfaz proporciona funciones de administración adicionales más allá de lo que es proporcionado por la herramienta de implementación de Office.
  
> [!NOTE]
> En este artículo se aplica a Office 2016 y versiones posteriores, Office 365. 
  
## <a name="integrating-with-the-click-to-run"></a>Integración con Click-to-Run

Para usar esta interfaz, una aplicación de la capacidad de administración invoca la interfaz COM y llamadas exponen las API que se comunican directamente con el servicio de instalación de Click-to-Run. 
  
> [!NOTE]
> El instalador de Office Click-to-Run se puede ejecutar desde la línea de comandos con parámetros que pueden controlar el comportamiento, tal como se documenta en [Office Deployment Tool for Click-to-Run](https://www.microsoft.com/en-us/download/details.aspx?id=49117). 
  
**A continuación se incluye un diagrama conceptual de la interfaz COM**

![Un diagrama del uso de la interfaz COM en el programa de instalación de Office Click-To-Run.] (media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "Un diagrama de uso de la interfaz COM en el programa de instalación de Office Click-To-Run")
  
La interfaz de Office 365 Click-to-Run installer implementa basada en COM, **IUpdateNotify** registrado para CLSID **CLSID_UpdateNotifyObject**.
  
Esta interfaz se puede invocar como sigue:
  
```cpp
hr = CoCreateInstance(CLSID_UpdateNotifyObject, NULL, CLSCTX_ALL,
       IID_IUpdateNotify, 
      (void **)&p); 
```

La llamada sólo funcionará correctamente si el autor de la llamada se ejecuta con privilegios elevados, como el programa de instalación de Click-to-Run se debe ejecutar con privilegios elevados.
  
La interfaz de **IUpdateNotify** COM expone tres funciones asincrónicas responsables de validar los comandos y parámetros y programación de ejecución con el servicio de instalación de Click-to-Run. 
  
```cpp
HRESULT Download([in] LPWSTR pcwszParameters) // Download update content.
HRESULT Apply([in] LPWSTR pcwszParameters) // Apply update content.
HRESULT Cancel() // Cancel the download action.

```

A otro método, **estado**, puede utilizarse para obtener información sobre el estado del último comando ejecutado o el estado del comando está ejecutando actualmente (es decir, correcto, error, códigos de error detallado).
  
```cpp
HRESULT status([out] _UPDATE_STATUS_REPORT* pUpdateStatusReport) // Get status of current action. 
typedef struct _UPDATE_STATUS_REPORT  
{  
UPDATE_STATUS status;  
UINT error; 
BSTR contentid;  
} UPDATE_STATUS_REPORT;

```

Existen cuatro estados que puede que el servicio de instalación de Click-to-Run en durante su ciclo de vida, durante el cual se pueden llamar a métodos de **IUpdateNotify** ; Reiniciar, inactivo, descargar y aplicar. 
  
**A continuación se incluye en el diagrama de máquina de estado de interfaz COM**

![Un diagrama de estado de la interfaz COM.] (media/a409003e-6876-4ab3-bb4c-cd0c0fed5cbb.png "Un diagrama de estado de la interfaz COM")
  
> [!NOTE]
> **Rebooting**: cuando se está iniciando la máquina hay un período de tiempo cuando el servicio de instalador de Click-to-Run no está disponible. Una llamada correcta al método estado después de un reinicio devolverá eUPDATE_UNKNOWN. 
  
**Inactividad:** Cuando el instalador de Click-to-Run está en el estado inactivo, se puede llamar: 
  
- **Aplicar**: instalar el contenido descargado previamente.
    
- **Cancelar**: devuelve `0x800000e`, "ha invocado un método en un momento imprevisto."
    
- **Descargar**: descarga nuevo contenido en el cliente para la instalación posterior.
    
- **Estado**: devuelve el resultado de la última acción completada o un mensaje de error si la acción se termina en error. Si no hay ninguna acción anterior, **estado** devuelve `eUPDATE_UNKNOWN`.
    
**Descargar:** Cuando el programa de instalación de Click-to-Run se encuentra en el estado de descarga, se puede llamar: 
  
- **Aplicar**: devuelve un **valor HRESULT** con el valor `0x800000e`, "ha invocado un método en un momento imprevisto."
    
- **Cancelar**: detiene la descarga y quita el contenido descargado parcialmente.
    
- **Descargar**: devuelve un **valor HRESULT** con el valor `0x800000e`, "ha invocado un método en un momento imprevisto." 
    
- **Estado**: devuelve **DOWNLOAD_WIP** para indicar que el trabajo de descarga está en curso. 
    
**Aplicar:** Cuando el instalador de Click-to-Run está en el proceso de instalación anteriormente descargar el contenido: 
  
- **Aplicar**: devuelve un **valor HRESULT** con el valor `0x800000e`, "ha invocado un método en un momento imprevisto."
    
- **Cancelar**: devuelve `0x800000e`, no se puede cancelar la acción de aplicar.
    
- **Descargar**: devuelve un **valor HRESULT** con el valor `0x800000e`, "ha invocado un método en un momento imprevisto." 
    
- **Estado**: devuelve **APPLY_WIP** para indicar que aplican trabajo está en curso. 
    
> [!NOTE]
> Puesto que OfficeC2RCOM es un servicio COM + y se carga dinámicamente, debe llamar a **CoCreateInstance** cada vez que se llame a un método en esta clase para garantizar que obtiene el resultado esperado. El servicio COM + controlará la creación de una nueva instancia si es necesario. Cuando se llama a uno de los métodos por primera vez, COM + va a cargar el objeto **IUpdateNotify** y ejecútelo dentro de una de las instancias de dllhost.exe. El nuevo objeto permanecerá activo para unos 3 minutos de inactividad. Si se realiza una llamada subsiguiente en tres minutos de la última llamada, el objeto **IUpdateNotify** permanecerá cargado y no se creará una nueva instancia. Si no la llamada se realiza en tres minutos, el objeto IUpdateNotify se descargará y se creará un nuevo objeto **IUpdateNotify** cuando se realiza la siguiente llamada. 
  
## <a name="click-to-run-installer-com-api-reference-guide"></a>Guía de referencia de API de COM de Click-to-Run installer

En la siguiente documentación de referencia de API:
  
- Los parámetros se encuentran en un formato de par clave/valor separado por un espacio.
    
- Los parámetros no distinguen mayúsculas de minúsculas.
    
- Hay una [lista de parámetros](https://blogs.technet.microsoft.com/odsupport/2014/03/03/the-new-update-now-feature-for-office-2013-click-to-run-for-office365-and-its-associated-command-line-and-switches/) con la documentación disponible. 
    
- Resumen de IUpdateNotify2 interfaz es ahora incluye.
    
### <a name="apply"></a>Apply

```cpp
HRESULT Apply([in] LPWSTR pcwszParameters) // Apply update content.
```

#### <a name="parameters"></a>Parameters

-  _nivel de presentación_: **true** para mostrar el estado de instalación, incluidos los errores, durante el proceso de actualización; **false** para ocultar el estado de la instalación, incluidos los errores, durante el proceso de actualización. El valor predeterminado es **false**.
    
-  _forceappshutdown_: **true** para forzar a las aplicaciones de Office para apagar inmediatamente cuando se desencadena la acción **Aplicar** ; **false** para producirá un error si se ejecutan las aplicaciones de Office. El valor predeterminado es **false**. Para obtener más información, vea la [sección Comentarios](#bk_ApplyRemark) . 
    
  Si se está ejecutando cualquier aplicación de Office cuando se desencadena la acción **Aplicar** , normalmente, se producirá un error de la acción **Aplicar** . Pasando `forceappshutdown=true` a la que **Aplicar** método hará que el servicio de **OfficeClickToRun** cerrar las aplicaciones y aplicar la actualización inmediatamente. El usuario puede experimentar pérdida de datos en este caso. 
    
#### <a name="return-results"></a>Devolver resultados

|||
|:-----|:-----|
|**S_OK** <br/> |Acción se envió correctamente al servicio de Click-To-Run para su ejecución.  <br/> |
|**E_ACCESSDENIED** <br/> |El autor de la llamada no se está ejecutando con privilegios elevados.  <br/> |
|**E_INVALIDARG** <br/> |Se han pasado parámetros no válidos.  <br/> |
|**E_ILLEGAL_METHOD_CALL** <br/> |Acción no está permitida en este momento. Para obtener más información, vea la [sección Comentarios](#bk_ApplyRemark) .  <br/> |

<a name="bk_ApplyRemark"></a>

#### <a name="remarks"></a>Observaciones

- Si se está ejecutando cualquier aplicación de Office cuando se desencadena la acción **Aplicar** , se producirá un error en la acción **Aplicar** . Pasando `forceappshutdown=true` a la que **Aplicar** método hará que el servicio de **OfficeClickToRun** cerrar inmediatamente a las aplicaciones de Office que se están ejecutando y aplican la actualización. El usuario puede experimentar datos tal como se les solicita no para guardar los cambios para abrir documentos.. 
    
- Esta acción sólo se puede desencadenar cuando el estado de COM es una de las siguientes opciones: 
    
  - **eUPDATE_UNKNOWN**
    
  - **eDOWNLOAD_CANCELLED**
    
  - **eDOWNLOAD_FAILED**
    
  - **eDOWNLOAD_SUCCEEDED**
    
  - **eAPPLY_SUCCEEDED**
    
  - **eAPPLY_FAILED**
    
- Si se llama el método **Apply** sin descargar el contenido anteriormente, el método **Apply** notificará **Succeeded** tal y como se ha detectado nada para aplicar y había completado correctamente el proceso de **aplicación** . 
    
### <a name="cancel"></a>Cancel

```cpp
HRESULT Cancel() // Cancel the download action.
```

#### <a name="return-results"></a>Devolver resultados

|||
|:-----|:-----|
|S_OK  <br/> |Acción se envió correctamente al servicio de Click-to-Run para su ejecución.  <br/> |
|E_ILLEGAL_METHOD_CALL  <br/> |Acción no está permitida en este momento. Vea la sección [comentarios](#bk_CancelRemarks) para obtener más información  <br/> |

<a name="bk_CancelRemarks"></a>

#### <a name="remarks"></a>Observaciones

- Este método sólo se puede desencadenar cuando el identificador de estado de COM **eDOWNLOAD_WIP**. Intentará cancelar la acción de descarga actual. El estado de COM se cambie a **eDOWNLOAD_CANCELLING** y finalmente, cambie a **eDOWNLOAD_CANCELED**. El estado de COM devolverá **E_ILLEGAL_METHOD_CALL** si se desencadena en cualquier otro momento. 
    
### <a name="download"></a>Descarga

```cpp
HRESULT Download([in] LPWSTR pcwszParameters) // Download update content.
```

#### <a name="parameters"></a>Parameters

-  _nivel de presentación_: **true** para mostrar el estado de instalación, incluidos los errores, durante el proceso de actualización; **false** para ocultar el estado de la instalación, incluidos los errores, durante el proceso de actualización. El valor predeterminado es **false**.
    
-  _updatebaseurl_: dirección URL para el origen de descarga alternativas.
    
-  _updatetoversion_: la versión para actualizar Office a. Defina este parámetro si desea actualizar a una versión anterior a la versión que está instalada actualmente.
    
-  _downloadsource_: el CLSID de la implementación personalizada de **IBackgroundCopyManager** (Administrador de BITS). 
    
-  _contentid_: identifica el contenido que desea descargar desde el servidor de contenido mediante el Administrador de BITS personalizado. Este valor se pasa a través de la interfaz de BITS para interpretación.
    
#### <a name="return-results"></a>Devolver resultados

|||
|:-----|:-----|
|**S_OK** <br/> |Acción se envió correctamente al servicio de Click-To-Run para su ejecución.  <br/> |
|**E_ACCESSDENIED** <br/> |El autor de la llamada no se está ejecutando con privilegios elevados.  <br/> |
|**E_INVALIDARG** <br/> |Se han pasado parámetros no válidos.  <br/> |
|**E_ILLEGAL_METHOD_CALL** <br/> |Acción no está permitida en este momento. Para obtener más información, vea la [sección Comentarios](#bk_DownloadRemark) .  <br/> |

<a name="bk_DownloadRemark"></a>

#### <a name="remarks"></a>Observaciones

- Debe especificar _downloadsource_ y _contentid_ como un par. En caso contrario, el método **Descargar** devolverá un error **E_INVALIDARG** . 
    
- Si se proporcionan _downloadsource_, _contentid_y _updatebaseurl_ , se omitirá _updatebaseurl_ . 
    
- Esta acción sólo se puede desencadenar cuando el estado de COM es una de las siguientes opciones: 
    
  - **eUPDATE_UNKNOWN**
    
  - **eDOWNLOAD_CANCELLED**
    
  - **eDOWNLOAD_FAILED**
    
  - **eDOWNLOAD_SUCCEEDED**
    
  - **eAPPLY_SUCCEEDED**
    
  - **eAPPLY_FAILED**
    
- Si se llama el método **Apply** sin contenido descargado anteriormente, el método **Apply se** notificará **Succeeded** tal y como se ha detectado nada para aplicar y había completado correctamente el proceso de **aplicación** . 
    
#### <a name="examples"></a>Ejemplos

- Para descargar el contenido desde el Administrador de BITS personalizado: llame a la función **download()** pasa los parámetros siguientes: 
    
  ```cpp
  "downloadsource=CLSIDofBITSInterface contentid=BITSServerContentIdentifier"
  ```

- Para descargar el contenido desde la CDN de Microsoft: llame a la función **download()** sin especificar los parámetros _downloadsource_, _contentid_o _updatebaseurl_ . 
    
- Para descargar el contenido desde una ubicación personalizada: llame a la función **download()** pasar el parámetro siguiente: 
    
  ```cpp
  "updatebaseurl=yourcontentserverurl"
  ```

### <a name="status"></a>Status

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
   
#### <a name="return-results"></a>Devolver resultados

|||
|:-----|:-----|
|**S_OK** <br/> |El método de **estado** siempre devuelve este resultado. Inspeccionar el `UPDATE_STATUS_RESULT` estructura para el estado de la acción actual.  <br/> |
   
#### <a name="remarks"></a>Observaciones

- El campo de estado de la `UPDATE_STATUS_REPORT` contiene el estado de la acción actual. Se devuelve uno de los siguientes valores de estado: 
    
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

- Si el último comando produjo un error, el campo de error de la `UPDATE_STATUS_REPORT` contiene información detallada sobre el error. Dos tipos de códigos de error se devuelven desde el método de **estado** . 
    
- Si el error inferior a `UPDATE_ERROR_CODE::eUNKNOWN`, el error es uno de los siguientes códigos de error predefinidos:
    
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

  Si el código de error devuelto es mayor que `UPDATE_ERROR_CODE::eUNKNOWN` es el **valor HRESULT** de una llamada de función con errores. Para extraer el HRESULT restar `UPDATE_ERROR_CODE::eUNKNOWN` desde el valor devuelto en el campo de error de la `UPDATE_STATUS_REPORT`.
    
  La lista completa de los valores de estado y error puede verse mediante la inspección de la biblioteca de tipos de **IUpdateNotify** incrustada en OfficeC2RCom.dll. 
    
- El campo contentid se usa para las llamadas al **estado de** después de **Descargar** ha iniciado y devuelve el contentid que se pasó a la llamada **Descargar** . Es una práctica recomendada para inicializar este campo en **null** antes de llamar al método de **estado** y, a continuación, compruebe el valor después de que se devuelva el **estado** . Si el valor sigue siendo **null**, que significa que no hay ningún contentid para devolver. Si el valor no es **null**, debe liberar con una llamada a **SysFreeString()**. Este es un fragmento de código de cómo llamar a **estado** después de **Descargar**.
    
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
> En este resumen se proporciona como una información en el complemento para [integrar las aplicaciones de la capacidad de administración con el programa de instalación de hacer clic y ejecutar de Office 365](https://msdn.microsoft.com/EN-US/library/office/mt608768.aspx). Una vez que se ha actualizado el doc pública, puede considerarse como obsoleto este doc. 
  
Desde C2RTenant [16.0.8208.6352](https://oloop/BuildGroup/Details/tenantc2rclient#3519/1255278) (primera generación públicamente disponible debe ser la compilación de horquilla junio--8326.*) hemos agregado una nueva interfaz de **IUpdateNotify2** . Aquí es algunos información básica acerca de esta interfaz: 
  
- CLSID_UpdateNotifyObject2, {52C2F9C2-F1AC-4021-BF50-756A5FA8DDFE}
    
- Esta interfaz también hospeda la interfaz de IUpdateNotify original para proporcionar compatibilidad con versiones anteriores. Lo que significa que si usa esta interfaz, tiene acceso a todos los métodos proporcionados en la interfaz de **UpdateNotifyObject** . 
    
- Nuevos métodos agregados a IUpdateNotify2:
    
  - **HRESULT** GetBlockingApps ([out] BSTR \* AppsList). Obtener actualizaciones de bloqueo de la lista de aplicaciones. Esta llamada devolverá la ejecución de aplicaciones de Office que se bloquea el proceso de actualización de continuar. 
    
  - **HRESULT** GetOfficeDeploymentData (tipo de datos int, pcwszName **LPCWSTR** , BSTR [out] [in] [in] * OfficeData). Obtener datos de implementación de Office. 
    
- Si desea utilizar los nuevos métodos, debe asegurarse de que:
    
  - La versión de C2R es más reciente que la compilación anterior (\>= compilación de horquilla de junio).
    
  - Use UpdateNotifyObject2, en lugar de **UpdateNotifyObject** para llamar a **CoCreateInstance**.
    
Si no usa cualquiera de los nuevos métodos, no es necesario cambiar nada. Todos los métodos existentes funcionará como exacta la misma manera que antes.
  
## <a name="implementing-the-bits-interface"></a>Implementación de la interfaz de BITS

El [Servicio de transferencia inteligente en segundo plano](https://msdn.microsoft.com/library/bb968799(v=vs.85).aspx) (BITS) es un servicio proporcionado por Microsoft para transferir archivos entre un cliente y un servidor. BITS es uno de los canales que puede usar el instalador de Office Click-To-Run para descargar el contenido. De forma predeterminada, la Office Click-To-Run installer usa las ventanas se basa en la implementación de BITS para descargar el contenido desde la CDN. 
  
Al proporcionar una implementación personalizada de BITS para el método **download()** de la interfaz de **IUpdateNotify** , el software de la capacidad de administración puede controlar dónde y cómo el cliente descarga el contenido. Una interfaz de BITS personalizada es útil cuando se proporciona un canal de distribución de contenido personalizados que no sean los canales de Click-to-Run integrados, como la CDN de Office, servidores IIS, o recursos compartidos de archivos. 
  
Es el requisito mínimo para una interfaz de BITS personalizada para que funcione con el servicio de Office C2R:
  
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

- Para el `Addfile` y `AddFileWithRanges` funciones, la dirección URL remota se encuentra en el siguiente formato: 
    
  ```cpp
  cmbits://<contentid>/<relative path to target file>
  ```

  - cmbits está codificado y el acrónimo en BITS personalizadas.
    
  -  _ \<contentid\> _ es el parámetro _contentid_ para el método **Download()** . 
    
  -  _ \<ruta de acceso relativa al archivo de destino\> _ proporciona el nombre de archivo y ubicación del archivo para descargar. 
    
    Por ejemplo, si ha proporcionado un _contentid_ de `f732af58-5d86-4299-abe9-7595c35136ef` a la **Download()** (método) y Office C2R desea descargar el archivo .cab de versión, como `v32.cab` archivo, llamará a **AddFile()** con el siguiente `RemoteUrl`:
    
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

## <a name="automating-content-staging"></a>Automatización de almacenamiento provisional de contenido

Los administradores de TI pueden elegir que los clientes de escritorio habilitados para recibir automáticamente actualizaciones cuando están disponibles directamente desde el Microsoft entrega red contenido (CDN) o pueden optar por controlar la implementación de actualizaciones disponibles en la actualización canales de uso de la herramienta de implementación de Office o System Center Configuration Manager.
  
El servicio admite la posibilidad de que las herramientas de administración para que reconozca y automatizar la descarga del contenido cuando se realicen actualizaciones disponibles.
  
**En la siguiente imagen es una visión general de la descarga de una imagen personalizada**

![Un diagrama del uso de la interfaz COM en el programa de instalación de Office Click-To-Run.] (media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "Un diagrama de uso de la interfaz COM en el programa de instalación de Office Click-To-Run")
  
### <a name="overview-of-downloading-a-custom-image"></a>Información general de la descarga de una imagen personalizada
  
En el diagrama anterior, verá que una nueva imagen de Office 365 ProPlus está disponible en la red de distribución de contenido (CDN) de Office. Junto con la imagen de Office 365 ProPlus, una lista de archivos con formato XML también está disponible que tiene la información necesaria para habilitar la capacidad de administración software crear directamente imágenes personalizadas reemplazando la necesidad de utilizar la herramienta de implementación de Office.
  
Una empresa configura sus WSUS para sincronizar las actualizaciones del cliente de Office 365. Estas actualizaciones no contienen la carga de la imagen real pero permitir que el software de la capacidad de administración reconocer al nuevo contenido está disponible. El software de la capacidad de administración, a continuación, puede leer los metadatos de actualización de cliente para comprender qué versión de Office que la actualización se aplica a.
  
Si la actualización es aplicable, el software de la capacidad de administración puede usar la lista de archivos y el contenido CDN para crear la imagen personalizada y almacenar en la ubicación del recurso compartido de archivo que está configurado para usar.
  
### <a name="format-of-the-xml-file-list"></a>Formato de la lista de archivos XML

Hay dos listas de archivos en un archivo cab en la CDN. Uno enumera los archivos de la versión de 32 bits de Office y otra para la versión de 64 bits de Office. La dirección URL de la ubicación de la lista de archivos de Office (OFL. Archivo CAB) es [https://officecdn.microsoft.com/pr/wsus/ofl.cab](https://officecdn.microsoft.com/pr/wsus/ofl.cab). Se llaman a las listas de dos archivos:
  
- O365Client_32bit.Xml
    
- O365Client_64bit.Xml
    
Dentro de XML para cada uno de los archivos está listas un <UpdateFiles> nodo que contiene un atributo de versión.  `<UpdateFiles version="1.4">`. Esta versión se incrementa si se realizan cambios en las listas de archivos.
  
Hay dos parámetros que se deben combinar con el código XML para que una imagen personalizada: 
  
- Reemplazar *% versión %* con la versión de compilación de Office. Esto se puede derivar de los metadatos de la actualización de cliente (que se explica en la siguiente sección). 
    
- Definir *URL base* mediante el valor de dirección URL asociado con la rama que se creó para la imagen. Esto se deriva de los metadatos de la actualización de cliente, que se explica en la sección siguiente. 
    
Los pasos para la creación de una imagen son:
  
1. Abra la lista de archivos XML.
    
2. Reemplace las apariciones de *% versión %* con la versión de compilación de Office aplicable. La versión de compilación se puede comprar desde releasehistory.xml tal como se describe más adelante en este artículo. 
    
3. Lea el atributo de dirección URL para la bifurcación de destino.
    
4. Quitar nodos de idioma para los idiomas que no es necesarios en la imagen personalizada.
    
   > [!NOTE]
   > Nodos con idioma = '0' son independientes del idioma y debe estar incluido en la imagen. 
  
5. Construir una imagen local de la red CDN iterar a través de la lista de archivos XML y copiar los archivos CDN, al crear la estructura de carpetas según sea necesario. 
    
   - Si se proporciona el atributo *rename* , a continuación, *cambie el nombre* proporcionado el archivo copiado en el valor en el atributo de cambio de nombre. Esto se usa para crear los archivos v64.cab y v32.cab de la predeterminada de nivel superior. Estas son las versiones ha cambiado el nombre del archivo cab de compilación de nivel superior y se usan como la versión de instalación predeterminada si no se especifica la versión. 
    
   - Use la dirección URL + relativePath + nombre de archivo para construir la ubicación CDN.
    
Los siguientes son ejemplos que usan el canal mensual (tal como se define por la `<baseURL>` nodo) y crear versión 16.0.4229.1004 desde releasehistory.xml. 
  
```xml
<baseURL branch="Monthly" URL="https://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60" />
```

- El siguiente es un archivo de idioma neutro necesario para todos los idiomas. El nombre del archivo es v64_16.0.4229.1004.cab y se debe copiar de `https://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/v64_16.0.4229.1004.cab` y cuyo nombre ha cambiado a `…/office/data/v64.cab`. 
    
  ```xml
  <File name="v64_%version%.cab" rename="v64.cab" relativePath="/office/data/" language="0"/>
  
  ```

- El siguiente es un archivo que se deben incluir en la imagen en-US como designado por el LCID del idioma = 1033. El nombre del archivo es s641033.cab y se debe copiar de `https://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/16.0.4229.1004/s641033.cab` y no cambia el nombre.
    
  ```xml
  <File name="s641033.cab" relativePath="/office/data/%version%/" language="1033" />
  ```

### <a name="hash-verification-of-dat-files"></a>Comprobación de hash de archivos .dat

Herramientas de creación de imagen pueden comprobar la integridad de los archivos .dat descargado mediante la comparación de un valor HASH calculado con el valor HASH proporcionado asociado con cada uno de los archivos .dat. Siguiente es un ejemplo de un archivo .dat del canal mensual con versión de compilación 16.0.4229.1004 y el idioma en búlgaro:
  
```xml
<File name="stream.x64.bg-bg.dat" hashLocation="s641026.cab/stream.x64.bg-bg.hash" hashAlgo="Sha256" relativePath="/office/data/%version%/" language="1026"/>
```

- El atributo **hashLocation** especifica la ubicación de la ruta de acceso relativa de la bg.hash stream.x64.bg para el archivo stream.x64.bg bg.dat. Construir la ubicación del archivo hash concatenando la dirección URL + relativePath + hashLocation. En el siguiente ejemplo, la ubicación de stream.x64.bg bg.hash sería: 
    
  ```http
  https://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/16.0.4229.1004/s641026.cab/stream.x64.bg-bg.hash 
  ```

- El atributo **hashAlgo** especifica qué algoritmo hash se usó. En este caso se usó Sha256. 
    
  Para validar la integridad del archivo stream.x64.bg-bg.dat, abra el bg.hash stream.x64.bg y leer el valor HASH que es la primera línea de texto en el archivo de hash. Compare esto con el valor hash calculado (mediante el algoritmo hash especificado) para comprobar la integridad del archivo .dat descargado.
    
  En el ejemplo siguiente se muestra el código de C# para leer el valor hash.
    
  ```cs
    string[] readHashes = System.IO.File.ReadAllLines(tmpFile, Encoding.Unicode);
    string readHash = readHashes.First();
  ```

### <a name="office-365-client-updates"></a>Actualizaciones de cliente de Office 365

Todas las actualizaciones de cliente de Office 365 se publican en el [Catálogo de Microsoft Update](https://www.catalog.update.microsoft.com/Search.aspx?q=office+365+client).
  
Actualizaciones de cliente de Office 365 permiten que el software de la capacidad de administración tratar las actualizaciones del cliente de Office 365 de manera muy similar a cualquier otra actualización WU con una excepción; las actualizaciones del cliente no contienen una carga real. No se debería instaladas en los clientes pero en su lugar se utiliza para activar los flujos de trabajo con el software de la capacidad de administración reemplazando el comando de instalación con COM según el mecanismo de instalación que se muestra encima de las actualizaciones del cliente de Office 365. 
  
**La siguiente ilustración muestra un diagrama de flujo de trabajo de actualización de cliente de Office 365.**

![Diagrama de flujo de trabajo para las actualizaciones del cliente de O365PP.] (media/bc8092b0-62b8-402c-a5c0-04d55cca01d4.png "Diagrama de flujo de trabajo para las actualizaciones del cliente de O365PP")
  
Cada Office 365 actualización de cliente que se publicará incluye metadatos acerca de la actualización. Estos metadatos incluyen un parámetro denominado *MoreInfoUrl* que se puede utilizar para derivar la siguiente información: 
  
-  *Ver*: identifica la versión de Office asociada con esta actualización. 
    
-  *Sucursal*: identifica el canal de actualización para esta actualización. Los valores son InsiderFast, personal, mensual, destino, Broad. Se pueden agregar a valores adicionales en el futuro. 
    
-  *Arco*: identifica la arquitectura del procesador asociada con esta actualización. 
    
-  *xmlVer*: la versión de las listas de archivos XML que se debe utilizar para construir la imagen base para esta actualización. 
    
-  *xmlPath*: ruta de acceso a la OFL. Muestra el archivo CAB que contiene el archivo XML. 
    
-  *mlFile*: el nombre de la lista de archivos que se debe usar para esta actualización. El valor será O365Client_32bit o O365Client_64bit y coincidirá con el arco. 
    
La siguiente dirección URL es un ejemplo del parámetro *MoreInfoURL* que hace referencia a las versiones de actualización de cliente de Office 365 para la versión de 32 bits de Office con la versión de compilación de 16.0.2342.2343 en el canal actual. 
  
https://officecdn.microsoft.com/pr/wsus/ofl.cabes la ubicación de las listas de archivo XML para esta actualización, específicamente la O365Client_32bit.xml desde dentro de la OFL. CAB.
  
[Versiones de canal de actualización de cliente de Office 365](https://go.microsoft.com/fwlink/?LinkId=626090&Ver=16.0.8326.2096&Branch=Current&Arch=64&XMLVer=1.4&xmlPath=https://officecdn.microsoft.com/pr/wsus/ofl.cab&xmlFile=O365Client_64bit.xml)
  
### <a name="additional-metadata-for-automating-content-staging"></a>Metadatos adicionales para automatizar el almacenamiento provisional de contenido

Además de los metadatos que se publicarán hay que define son archivos XML adicionales publicar también a la CDN que puede ayudar a proporcionar información adicional acerca de los clientes de Office 365 que están disponibles desde la CDN de Office.
  
**SKU. XML**
  
Este archivo XML está contenido dentro de un archivo CAB firmado y publicado en la CDN de Office en la siguiente dirección URL: [https://officecdn.microsoft.com/pr/wsus/skus.cab](https://officecdn.microsoft.com/pr/wsus/skus.cab).
  
Los metadatos que se publican en este archivo XML están útil para determinar qué productos están disponibles para la implementación y la atención desde la CDN de Office junto con distintas opciones para cada uno. 
  
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

** \<ReleaseInfo\> ** nodo raíz contiene el atributo PublishedDate que identifica la fecha que se publicó este archivo. 
  
** \<SKU\> ** nodo identifica un SKU individual. 
  
- El atributo *ProductID* identifica el identificador que se pasa como el atributo ID en el configuration.xml si usa la ODT. Por ejemplo, `<Product ID="O365ProPlusRetail">`. 
    
- El *valor predeterminado* de atributo, si establece en True, identifica la SKU recomendado. 
    
** \<Aplicación\> ** nodos se usan para definir las aplicaciones individuales de Office que admite cada SKU. 
  
- El atributo *Name* es el nombre de la aplicación que se muestra. 
    
- El atributo *AppID* es el atributo ID se pasan en la configuration.xml para el ** \<ExcludeApp\> ** nodo si usa la ODT. Por ejemplo, `<ExcludeApp ID="Publisher" />`. 
    
**RELEASEHISTORY. XML**
  
Este archivo XML está contenido dentro de un archivo CAB firmado y publicado en la CDN de Office en la siguiente ubicación: [https://officecdn.microsoft.com/pr/wsus/releasehistory.cab](https://officecdn.microsoft.com/pr/wsus/releasehistory.cab). 
  
Los metadatos que se publican en este archivo XML están útil para determinar qué canales se admiten para el mantenimiento de las actualizaciones desde la CDN de Office junto con información sobre el historial de compilación para cada uno de los canales compatibles.
  
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

La ** \<ReleaseHistory\> ** nodo raíz contiene el atributo PublishedDate que identifica la fecha que se publicó este archivo. 
  
La ** \<UpdateChannel\> ** nodo define un canal compatible. 
  
- El atributo *Name* define el identificador de canal que se usa para pasar a la ODT en la configuration.xml como el atributo de canal. 
    
  Ejemplo: `<Add SourcePath="\\Server\Share" OfficeClientEdition="32" Channel="Current">` 
    
  > [!NOTE] 
  > Este atributo está desusado y se usa para la compatibilidad con versiones anteriores. Use el atributo de identificador en lugar del atributo de nombre. 
    
- El atributo *ID* define el identificador de canal que se usa para pasar a la ODT en la configuration.xml como el atributo de canal. 
    
  Ejemplo: `<Add SourcePath="\\Server\Share" OfficeClientEdition="32" Channel="Deferred">` 
    
- El atributo **DisplayName** se utiliza como el nombre para mostrar. 
    
La ** \<actualizar\> ** nodo se usa para definir cada actualización que se ha publicado para ese canal en concreto. 
  
- Atributo la **más reciente** , si establece en True, se define la versión que es la versión más reciente para ese canal. 
    
- El atributo de **versión** define el número de versión para esta actualización determinado. 
    
- El atributo **LegacyVersion** define el número de versión completa para esta actualización determinado. 
    
- El atributo **crear** define el número de compilación para esta actualización determinado. 
    
- El atributo **PubTime** define la fecha y hora en que esta actualización se ha publicado en la CDN de Office. 
    

