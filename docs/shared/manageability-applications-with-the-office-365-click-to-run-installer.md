---
title: Integración de aplicaciones de administración con el instalador de hacer clic y ejecutar de Microsoft 365 aplicaciones
manager: lindalu
ms.date: 09/28/2020
ms.audience: ITPro
localization_priority: Normal
ms.assetid: c0fa8fed-1585-4566-a9be-ef6d6d1b4ce8
description: Obtenga información sobre cómo integrar el instalador de hacer clic y ejecutar de Microsoft 365 apps con una solución de administración de software.
ms.openlocfilehash: eccd634f7906acf25b521ed2deb456ca914f37da
ms.sourcegitcommit: c8c51bd3f51c0a59fe44c014c8e56f1ba7c7aa03
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2020
ms.locfileid: "48297317"
---
# <a name="integrating-manageability-applications-with-microsoft-365-apps-click-to-run-installer"></a>Integración de aplicaciones de administración con el instalador de hacer clic y ejecutar de Microsoft 365 aplicaciones

Obtenga información sobre cómo integrar el instalador de hacer clic y ejecutar de Microsoft 365 apps con una solución de administración de software.
  
El instalador de hacer clic y ejecutar de Microsoft 365 apps proporciona una interfaz COM que permite a los profesionales de ti y a las soluciones de administración de software controlar mediante programación la administración de actualizaciones. Esta interfaz proporciona funciones de administración adicionales más allá de lo que proporciona la herramienta de implementación de Office.
  
> [!NOTE]
> Este artículo se aplica a las aplicaciones de Office que usan el instalador de hacer clic y ejecutar. 
  
## <a name="integrating-with-the-click-to-run"></a>Integración con hacer clic y ejecutar

Para usar esta interfaz, una aplicación de administración invoca la interfaz COM y llama a las API expuestas que se comunican directamente con el servicio de instalación de hacer clic y ejecutar. 
  
> [!NOTE]
> El instalador de hacer clic y ejecutar de Office puede ejecutarse desde la línea de comandos con parámetros que pueden controlar el comportamiento, tal como se documenta en la [herramienta de implementación de Office para hacer clic y ejecutar](https://docs.microsoft.com/DeployOffice/overview-office-deployment-tool). 
  
**A continuación se encuentra un diagrama conceptual de la interfaz COM**

![Diagrama del uso de la interfaz COM en el programa de instalación de Hacer clic y ejecutar de Office.](media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "Diagrama de uso de la interfaz COM en el instalador de hacer clic y ejecutar de Office")
  
El instalador de hacer clic y ejecutar de Microsoft 365 apps implementa una interfaz basada en COM, **IUpdateNotify** registrada en CLSID **CLSID_UpdateNotifyObject**.
  
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

Hay cuatro Estados en los que el servicio de instalación de hacer clic y ejecutar puede encontrarse durante su ciclo de vida, durante el cual se puede llamar a los métodos de **IUpdateNotify** ; Reiniciar, inactivo, descargar y aplicar. 
  
**A continuación se encuentra el diagrama de máquina de estado de interfaz COM**

![Un diagrama de estado de la interfaz COM.](media/a409003e-6876-4ab3-bb4c-cd0c0fed5cbb.png "Un diagrama de estado para la interfaz COM")
  
> [!NOTE]
> **Reiniciar**: cuando el equipo arranca, hay un período de tiempo en el que el servicio de instalación de hacer clic y ejecutar no está disponible. Una llamada correcta al método de estado después de un reinicio, devolverá eUPDATE_UNKNOWN. 
  
**Inactivo:** Cuando el programa de instalación de hacer clic y ejecutar se encuentra en estado inactivo, puede llamar a: 
  
- **Aplicar**: instalar contenido descargado anteriormente.
    
- **Cancel**: devuelve  `0x800000e` "se llamó a un método en un momento inesperado".
    
- **Descargar**: descarga nuevo contenido en el cliente para su instalación posterior.
    
- **Status**: devuelve el resultado de la última acción completada o un mensaje de error si la acción finalizó por error. Si no hay ninguna acción anterior, **status** devuelve  `eUPDATE_UNKNOWN` .
    
**Descargar:** Cuando el programa de instalación de hacer clic y ejecutar se encuentra en estado de descarga, puede llamar a: 
  
- **Apply**: devuelve un **HRESULT** con el valor  `0x800000e` , "se llamó a un método en un momento inesperado".
    
- **Cancelar**: detiene la descarga y quita el contenido parcialmente descargado.
    
- **Download**: devuelve un **HRESULT** con el valor  `0x800000e` "se llamó a un método en un momento inesperado". 
    
- **Status**: devuelve **DOWNLOAD_WIP** para indicar que el trabajo de descarga está en curso. 
    
**Aplicar:** Cuando el programa de instalación de hacer clic y ejecutar está en proceso de instalar contenido de descarga anterior: 
  
- **Apply**: devuelve un **HRESULT** con el valor  `0x800000e` , "se llamó a un método en un momento inesperado".
    
- **Cancelar**: devuelve  `0x800000e` , la acción Apply no se puede cancelar.
    
- **Download**: devuelve un **HRESULT** con el valor  `0x800000e` "se llamó a un método en un momento inesperado". 
    
- **Status**: devuelve **APPLY_WIP** para indicar que el trabajo de aplicación está en curso. 
    
> [!NOTE]
> Dado que OfficeC2RCOM es un servicio COM+ y se carga dinámicamente, es necesario llamar a **CoCreateInstance** cada vez que se llama a un método en esta clase para garantizar que se obtiene el resultado esperado. El servicio COM+ administrará la creación de una nueva instancia si es necesario. Cuando se llama a uno de los métodos por primera vez, COM+ cargará el objeto **IUpdateNotify** y lo ejecutará dentro de una de las instancias de dllhost.exe. El nuevo objeto permanecerá activo durante unos 3 minutos de inactividad. Si se realiza una llamada subsiguiente en tres minutos después de la última llamada, el objeto **IUpdateNotify** permanecerá cargado y no se creará una nueva instancia. Si no se realiza ninguna llamada en un plazo de tres minutos, el objeto IUpdateNotify se descargará y se creará un nuevo objeto **IUpdateNotify** cuando se realice la siguiente llamada. 
  
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

#### <a name="parameters"></a>Parámetros

-  _displaylevel_: **true** para mostrar el estado de la instalación, incluidos los errores, durante el proceso de actualización; **false** para ocultar el estado de la instalación, incluidos los errores, durante el proceso de actualización. El valor predeterminado es **false**.
    
-  _forceappshutdown_: **true** para forzar que las aplicaciones de Office se cierren inmediatamente cuando se desencadena la acción **Apply** ; **false** se producirá un error si se ejecuta cualquier aplicación de Office. El valor predeterminado es **false**. Vea los [comentarios](#bk_ApplyRemark) para obtener más información. 
    
  Si se está ejecutando cualquier aplicación de Office cuando se desencadena la acción **Apply** , la acción **Apply** producirá un error. Pasar  `forceappshutdown=true` al método **Apply** hará que el servicio **OfficeClickToRun** cierre inmediatamente las aplicaciones y aplique la actualización. En este caso, el usuario puede experimentar pérdida de datos. 
    
#### <a name="return-results"></a>Resultados devueltos

|||
|:-----|:-----|
|**S_OK** <br/> |La acción se ha enviado correctamente al servicio de hacer clic y ejecutar para su ejecución.  <br/> |
|**E_ACCESSDENIED** <br/> |El autor de la llamada no se está ejecutando con privilegios elevados.  <br/> |
|**E_INVALIDARG** <br/> |Se pasaron parámetros no válidos.  <br/> |
|**E_ILLEGAL_METHOD_CALL** <br/> |La acción no está permitida en este momento. Vea los [comentarios](#bk_ApplyRemark) para obtener más información.  <br/> |

<a name="bk_ApplyRemark"></a>

#### <a name="remarks"></a>Comentarios

- Si se está ejecutando cualquier aplicación de Office cuando se desencadena la acción **Apply** , se producirá un error en la acción **Apply** . Pasar  `forceappshutdown=true` al método **Apply** hará que el servicio **OfficeClickToRun** cierre inmediatamente todas las aplicaciones de Office que se estén ejecutando y aplique la actualización. El usuario puede experimentar datos porque no se le pide que guarde los cambios realizados en los documentos abiertos. 
    
- Esta acción solo se puede desencadenar cuando el estado de COM es uno de los siguientes: 
    
  - **eUPDATE_UNKNOWN**
    
  - **eDOWNLOAD_CANCELLED**
    
  - **eDOWNLOAD_FAILED**
    
  - **eDOWNLOAD_SUCCEEDED**
    
  - **eAPPLY_SUCCEEDED**
    
  - **eAPPLY_FAILED**
    
- Si se llama al método **Apply** sin descargar previamente el contenido, el método **Apply** notificará que el proceso se ha **realizado** correctamente, ya que se ha detectado que no se ha aplicado nada y que se ha completado el proceso de **aplicación** . 
    
### <a name="cancel"></a>Cancelar

```cpp
HRESULT Cancel() // Cancel the download action.
```

#### <a name="return-results"></a>Resultados devueltos

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

#### <a name="parameters"></a>Parámetros

-  _displaylevel_: **true** para mostrar el estado de la instalación, incluidos los errores, durante el proceso de actualización; **false** para ocultar el estado de la instalación, incluidos los errores, durante el proceso de actualización. El valor predeterminado es **false**.
    
-  _updatebaseurl_: dirección URL al origen de descarga alternativo.
    
-  _updatetoversion_: versión en la que se va a actualizar Office. Defina este parámetro si desea actualizar a una versión anterior a la versión instalada actualmente.
    
-  _downloadsource_: CLSID de la implementación de **IBackgroundCopyManager** personalizada (Administrador de bits). 
    
-  _contentid_: identifica el contenido que se va a descargar desde el servidor de contenido mediante el administrador de bits personalizado. Este valor se pasa a través de la interfaz de BITS para la interpretación.
    
#### <a name="return-results"></a>Resultados devueltos

|||
|:-----|:-----|
|**S_OK** <br/> |La acción se ha enviado correctamente al servicio de hacer clic y ejecutar para su ejecución.  <br/> |
|**E_ACCESSDENIED** <br/> |El autor de la llamada no se está ejecutando con privilegios elevados.  <br/> |
|**E_INVALIDARG** <br/> |Se pasaron parámetros no válidos.  <br/> |
|**E_ILLEGAL_METHOD_CALL** <br/> |La acción no está permitida en este momento. Vea los [comentarios](#bk_DownloadRemark) para obtener más información.  <br/> |

<a name="bk_DownloadRemark"></a>

#### <a name="remarks"></a>Comentarios

- Debe especificar  _downloadsource_ y  _contentid_ como un par. De lo contrario, el método de **descarga** devolverá un error de **E_INVALIDARG** . 
    
- Si se proporciona  _downloadsource_,  _contentid_y  _updatebaseurl_ , se omitirá  _updatebaseurl_ . 
    
- Esta acción solo se puede desencadenar cuando el estado de COM es uno de los siguientes: 
    
  - **eUPDATE_UNKNOWN**
    
  - **eDOWNLOAD_CANCELLED**
    
  - **eDOWNLOAD_FAILED**
    
  - **eDOWNLOAD_SUCCEEDED**
    
  - **eAPPLY_SUCCEEDED**
    
  - **eAPPLY_FAILED**
    
- Si se llama al método **Apply** sin descargar previamente el contenido, el método **Apply** informará de que el proceso se ha detectado correctamente **, ya que** se ha detectado que no se ha aplicado nada y se ha completado el proceso de **aplicación** . 
    
#### <a name="examples"></a>Ejemplos

- Para descargar el contenido del administrador de BITS personalizado: llame a la función **download ()** y pase los siguientes parámetros: 
    
  ```cpp
  "downloadsource=CLSIDofBITSInterface contentid=BITSServerContentIdentifier"
  ```

- Para descargar el contenido de la red de entrega de contenido (CDN) de Office: llame a la función **download ()** sin especificar los parámetros  _downloadsource_,  _contentid_o  _updatebaseurl_ . 
    
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

#### <a name="parameters"></a>Parámetros

|||
|:-----|:-----|
| _pUpdateStatusReport_ <br/> |Puntero a una estructura UPDATE_STATUS_REPORT.  <br/> |
   
#### <a name="return-results"></a>Resultados devueltos

|||
|:-----|:-----|
|**S_OK** <br/> |El método **status** siempre devuelve este resultado. Inspeccione la  `UPDATE_STATUS_RESULT` estructura del estado de la acción actual.  <br/> |
   
#### <a name="remarks"></a>Comentarios

- El campo Estado de  `UPDATE_STATUS_REPORT` contiene el estado de la acción actual. Se devuelve uno de los siguientes valores de estado: 
    
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

- Si se produce un error en el último comando, el campo de error del  `UPDATE_STATUS_REPORT` contiene información detallada sobre el error. Se devuelven dos tipos de códigos de error del método **status** . 
    
- Si el error es menor que  `UPDATE_ERROR_CODE::eUNKNOWN` , el error es uno de los siguientes códigos de error predefinidos:
    
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

  Si el código de error devuelto es mayor que  `UPDATE_ERROR_CODE::eUNKNOWN` el **valor HRESULT** de una llamada a una función fallida. Para extraer el valor de resta de HRESULT del  `UPDATE_ERROR_CODE::eUNKNOWN` valor devuelto en el campo de error del  `UPDATE_STATUS_REPORT` .
    
  Para ver la lista completa de valores de estado y error, inspeccione la biblioteca de tipos de **IUpdateNotify** incrustada en OfficeC2RCom.dll. 
    
- El campo contentid se usa para las llamadas al **Estado** una vez iniciada la **descarga** y devuelve el elemento contentid que se pasó a la llamada a **download** . Se recomienda inicializar este campo en **null** antes de llamar al método **status** y, a continuación, comprobar el valor una vez que se ha devuelto el **Estado** . Si el valor todavía es **null**, significa que no hay contentid para devolver. Si el valor no es **null**, debe liberarlo con una llamada a **SysFreeString ()**. A continuación, se muestra un fragmento de código sobre cómo llamar al **Estado** después de la **descarga**.
    
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

Desde la versión [16.0.8208.6352] hemos agregado una nueva interfaz de **IUpdateNotify2** . 
  
- CLSID_UpdateNotifyObject2, {52C2F9C2-F1AC-4021-BF50-756A5FA8DDFE}
    
- Esta interfaz también hospedaba la interfaz IUpdateNotify original para proporcionar compatibilidad con versiones anteriores. Lo que significa que si usa esta interfaz, tiene acceso a todos los métodos proporcionados en la interfaz **UpdateNotifyObject** . 
    
- Nuevos métodos agregados a IUpdateNotify2:
    
  - **HRESULT** GetBlockingApps ([salida] BSTR \* AppsList). Obtener actualizaciones bloqueo de la lista de aplicaciones. Esta llamada devolverá la ejecución de aplicaciones de Office que impedirán que el proceso de actualización continúe. 
    
  - **HRESULT** GetOfficeDeploymentData ([in] int DataType, [in] **LPCWSTR** pcwszName, [out] BSTR * OfficeData). Obtener datos de implementación de Office. 
    
- Si desea usar los nuevos métodos, debe asegurarse de lo siguiente:
    
  - La versión de C2R es más reciente que la compilación anterior ( \> = compilación de la bifurcación de junio).
    
  - Use UpdateNotifyObject2, en lugar de **UpdateNotifyObject** para llamar a **CoCreateInstance**.
    
Si no usa ninguno de los métodos nuevos, no es necesario cambiar nada. Todos los métodos existentes funcionarán exactamente del mismo modo que antes.
  
## <a name="implementing-the-bits-interface"></a>Implementación de la interfaz de BITS

El [servicio de transferencia inteligente en segundo plano](https://docs.microsoft.com/windows/win32/bits/background-intelligent-transfer-service-portal) (bits) es un servicio proporcionado por Microsoft para transferir archivos entre un cliente y un servidor. BITS es uno de los canales que puede usar el instalador de hacer clic y ejecutar de Office para descargar contenido. De forma predeterminada, el instalador de hacer clic y ejecutar de Microsoft 365 apps usa la implementación integrada de BITS de Windows para descargar el contenido de la red CDN. 
  
Al suministrar una implementación BITS personalizada al método **download ()** de la interfaz **IUpdateNotify** , el software de administración puede controlar dónde y cómo descarga el contenido el cliente. Una interfaz de BITS personalizada es útil cuando se proporciona un canal de distribución de contenido personalizado distinto de los canales integrados de hacer clic y ejecutar, como la red CDN, los servidores IIS o los recursos compartidos de archivos. 
  
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

- Para las  `Addfile`  `AddFileWithRanges` funciones y, la dirección URL remota tiene el siguiente formato: 
    
  ```cpp
  cmbits://<contentid>/<relative path to target file>
  ```

  - cmbits está codificado de forma rígida y representa BITS personalizados.
    
  -  _\<contentid\>_ es el parámetro  _contentid_ del método **download ()** . 
    
  -  _\<relative path to target file\>_ proporciona la ubicación y el nombre del archivo que se va a descargar. 
    
    Por ejemplo, si ha proporcionado un  _contentid_ del  `f732af58-5d86-4299-abe9-7595c35136ef` al método **download ()** y Office C2R desea descargar el archivo CAB de la versión, como  `v32.cab` File, llamará a **AddFile ()** con lo siguiente  `RemoteUrl` :
    
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
## <a name="automating-content-staging"></a>Automatizar el almacenamiento provisional del contenido

Los administradores de TI pueden elegir que los clientes de escritorio reciban automáticamente actualizaciones cuando están disponibles directamente desde la red CDN o pueden elegir controlar la implementación de las actualizaciones disponibles en los canales de actualización mediante la herramienta de implementación de Office o el administrador de configuración de Microsoft Endpoint.
  
El servicio admite la capacidad de las herramientas de administración para reconocer y automatizar la descarga del contenido cuando las actualizaciones estén disponibles.
  
**La siguiente imagen es una introducción a la descarga de una imagen personalizada**

![Diagrama del uso de la interfaz COM en el programa de instalación de Hacer clic y ejecutar de Office.](media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "Diagrama de uso de la interfaz COM en el instalador de hacer clic y ejecutar de Office")
  
### <a name="overview-of-downloading-a-custom-image"></a>Información general sobre la descarga de una imagen personalizada
  
En el diagrama anterior, verá que una nueva imagen de Microsoft 365 de aplicaciones está disponible en la red CDN. Junto con la imagen de aplicaciones de Microsoft 365, hay disponible una API que tiene la información necesaria para permitir que el software de administración pueda crear imágenes personalizadas directamente, lo que reemplaza la necesidad de usar la herramienta de implementación de Office.

Una empresa configura su WSUS para que sincronice las actualizaciones de las aplicaciones de Microsoft 365. Estas actualizaciones no contienen la carga real de la imagen, pero sí permiten que el software de administración reconozca cuando hay contenido nuevo disponible. El software de administración puede leer los metadatos de la actualización de aplicaciones de Microsoft 365 para comprender a qué versión de Office se aplica la actualización.

Si la actualización es aplicable, el software de administración puede usar el contenido de la red CDN y la lista de archivos para crear la imagen personalizada y almacenarla en la ubicación del recurso compartido de archivos que está configurada para usar.
  
### <a name="using-the-microsoft-365-apps-file-list-api"></a>Uso de la API de lista de archivos de aplicaciones de 365 de Microsoft

La API de la lista de archivos de aplicaciones de Microsoft 365 se usa para recuperar los nombres de los archivos necesarios para una actualización de aplicaciones 365 de Microsoft en particular.

Solicitud HTTP

GET https://config.office.com/api/filelist

No proporcione un cuerpo de solicitud para este método.

No se necesitan permisos para llamar a esta API.

Parámetros de consulta opcionales

|**Name**|**Descripción**|
|:-----|:-----|
| channel <br/>| Especifica el nombre del canal.  <br/> Opcional: valor predeterminado en "semestral" <br/> Valores admitidos https://docs.microsoft.com/DeployOffice/office-deployment-tool-configuration-options#channel-attribute-part-of-add-element |
| version <br/>| Especifica la versión de actualización <br/> Optional: valor predeterminado para la versión más reciente disponible para el canal especificado |
| engloba <br/>| Especifica la arquitectura del cliente <br/> Optional: predeterminado para ' x64 ' <br/> Valores admitidos: x64, x86 |
| lid <br/>| Especifica los archivos de idioma que se van a incluir <br/> Opcional: el valor predeterminado es None <br/> Para especificar varios idiomas, incluya un parámetro de consulta de la tapa para cada idioma <br/> Use el formato de identificador de idioma, por ejemplo, "en-US", "fr-fr" |
| alllanguages <br/>| Especifica que se incluyan todos los archivos de idioma <br/> Opcional: el valor predeterminado es false. |

Respuesta HTTP

Si se ejecuta correctamente, este método devuelve un código de respuesta 200 correcto y la colección de objetos File en el cuerpo de la respuesta.

Para crear una imagen, siga estos pasos:
1.  Llame a la API y proporcione los parámetros de consulta apropiados para el canal, la versión y la arquitectura de la actualización que le interesa.
Nota: los objetos file con el atributo "LCID": "0" son archivos independientes del idioma y deben incluirse en la imagen.
2.  Construya una imagen local de la red CDN iterando por los objetos de archivo y copiando los archivos de la red CDN, a la vez que crea la estructura de carpetas especificada por el atributo "relativePath" definido para cada uno de los objetos de archivo.

En el ejemplo siguiente se recupera la lista de archivos para el canal actual y la versión 16.0.4229.1004 para 64 bits, y se incluyen los archivos de idioma francés e inglés:

```http
Get https://config.office.com/api/filelist?Channel=Current&Version=16.0.4229.1004&Arch=x64&Lid=fr-fr&Lid=en-US
```

### <a name="hash-verification-of-dat-files"></a>Comprobación de hash de los archivos. dat

Las herramientas de creación de imágenes pueden comprobar la integridad de los archivos. dat descargados mediante la comparación de un valor hash calculado con el valor hash proporcionado asociado con cada uno de los archivos. dat. A continuación se indica un ejemplo de un objeto File que especifica los valores hashLocation y hashAlgorithm:
  
```xml
{
  "url": "https://officecdn.microsoft.com/pr/7ffbc6bf-bc32-4f92-8982-f9dd17fd3114/office/data/16.0.1234.1001/stream.x64.x-none.dat",
  "name": "stream.x64.x-none.dat",
  "relativePath": "/office/data/16.0.1234.1001/",
  "hashLocation": "s640.cab/stream.x64.x-none.hash",
  "hashAlgorithm": "Sha256",
  "lcid": "0"
},
```

- El atributo **hashLocation** especifica la ubicación de la ruta de acceso relativa del archivo. cab que contiene el valor hash. Construya la ubicación del archivo hash concatenando la dirección URL + relativePath + hashLocation. En el siguiente ejemplo, la ubicación de stream.x64.bg-BG. hash sería: 
    
  ```http
  https://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/16.0.4229.1004/s641026.cab/stream.x64.bg-bg.hash 
  ```

- El atributo **hashAlgorithm** especifica el algoritmo hash que se usó. 
    
  Para validar la integridad del archivo stream.x64.bg-BG. dat, abra el stream.x64.bg-BG. hash y lea el valor de HASH, que es la primera línea de texto del archivo hash. Compare esto con el valor hash calculado (con el algoritmo hash especificado) para comprobar la integridad del archivo. dat descargado.
    
  En el ejemplo siguiente se muestra el código de C# para leer el hash.
    
  ```cs
    string[] readHashes = System.IO.File.ReadAllLines(tmpFile, Encoding.Unicode);
    string readHash = readHashes.First();
  ```

### <a name="microsoft-365-apps-updates"></a>Actualizaciones de Microsoft 365 apps

Todas las actualizaciones de Microsoft 365 apps se publican en el [Catálogo de Microsoft Update](https://www.catalog.update.microsoft.com/Search.aspx?q=office+365+client).
  
Las actualizaciones de Microsoft 365 apps habilitan el software de administración para tratar las actualizaciones de las aplicaciones de Microsoft 365 de una manera similar a cualquier otra actualización de WU con una excepción; las actualizaciones de cliente no contienen una carga real. Las actualizaciones de Microsoft 365 apps no deben instalarse en ningún cliente, sino que se usan para desencadenar flujos de trabajo con el software de administración que reemplaza el comando de instalación por el mecanismo de instalación basado en COM mostrado anteriormente.

**En la siguiente figura se muestra un diagrama del flujo de trabajo de actualización de cliente de Office 365.**

![Diagrama de flujo de trabajo para las actualizaciones de cliente de O365PP.](media/bc8092b0-62b8-402c-a5c0-04d55cca01d4.png "Diagrama de flujo de trabajo para actualizaciones de cliente de O365PP")
  
Cada actualización de Microsoft 365 apps publicada incluye metadatos sobre la actualización. Estos metadatos incluyen un parámetro denominado MoreInfoUrl que se puede usar para derivar la llamada a la API en la API de la lista de archivos para esa actualización específica.

En el siguiente ejemplo, la API de la lista de archivos se inserta en el MoreInfoURL y empieza por "ServicePath =".

http://go.microsoft.com/fwlink/?LinkId=626090&Ver=16.0.12527.21104&Branch=Insiders&Arch=64&XMLVer=1.6&xmlPath=http://officecdn.microsoft.com/pr/wsus/ofl.cab&xmlFile=O365Client_64bit.xml& ServicePath =https://config.office.com/api/filelist?Channel=Insiders&Version=16.0.12527.21104&Arch=64&AllLanguages=True
  
### <a name="additional-metadata-for-automating-content-staging"></a>Metadatos adicionales para automatizar el contenido provisional

**API del historial de versiones**
  
La API de historial de lanzamiento de aplicaciones de Microsoft 365 se usa para recuperar los detalles de cada una de las actualizaciones publicadas en la red CDN junto con los nombres de canal y otros atributos de canal.

Solicitud HTTP

```http
GET https://config.office.com/api/filelist/channels 
```

No proporcione un cuerpo de solicitud para este método.

No se necesitan permisos para llamar a esta API.

Respuesta HTTP

Si se ejecuta correctamente, este método devuelve un código de respuesta 200 correcto y la colección de objetos File en el cuerpo de la respuesta.

**API de SKU**
  
La API de SKU devuelve información útil para determinar qué productos están disponibles para su implementación y mantenimiento desde la red CDN de Office junto con varias opciones para cada uno.

Solicitud HTTP

```http
GET https://config.office.com/api/filelist/skus 
```

No proporcione un cuerpo de solicitud para este método.

No se necesitan permisos para llamar a esta API.

Respuesta HTTP

Si se ejecuta correctamente, este método devuelve un código de respuesta 200 correcto y la colección de objetos File en el cuerpo de la respuesta.
