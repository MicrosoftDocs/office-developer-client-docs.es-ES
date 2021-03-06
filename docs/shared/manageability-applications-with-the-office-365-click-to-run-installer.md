---
title: Integración de aplicaciones de administración con Aplicaciones Microsoft 365 instalador hacer clic y ejecutar
manager: lindalu
ms.date: 09/28/2020
ms.audience: ITPro
localization_priority: Normal
ms.assetid: c0fa8fed-1585-4566-a9be-ef6d6d1b4ce8
description: Obtenga información sobre cómo integrar el Aplicaciones Microsoft 365 de hacer clic y ejecutar con una solución de administración de software.
ms.openlocfilehash: eccd634f7906acf25b521ed2deb456ca914f37da
ms.sourcegitcommit: c8c51bd3f51c0a59fe44c014c8e56f1ba7c7aa03
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2020
ms.locfileid: "48297317"
---
# <a name="integrating-manageability-applications-with-microsoft-365-apps-click-to-run-installer"></a>Integración de aplicaciones de administración con Aplicaciones Microsoft 365 instalador hacer clic y ejecutar

Obtenga información sobre cómo integrar el Aplicaciones Microsoft 365 de hacer clic y ejecutar con una solución de administración de software.
  
El Aplicaciones Microsoft 365 hacer clic y ejecutar proporciona una interfaz COM que permite a los profesionales de IT y a las soluciones de administración de software controlar mediante programación la administración de actualizaciones. Esta interfaz proporciona capacidades de administración adicionales más allá de lo que proporciona la Office de implementación.
  
> [!NOTE]
> Este artículo se aplica a Office aplicaciones que usan el instalador Hacer clic y ejecutar. 
  
## <a name="integrating-with-the-click-to-run"></a>Integración con el botón Hacer clic y ejecutar

Para usar esta interfaz, una aplicación de facilidad de administración invoca la interfaz COM y llama a las API expuestas que se comunican directamente con el servicio de instalación Hacer clic y ejecutar. 
  
> [!NOTE]
> El instalador Office hacer clic y ejecutar se puede ejecutar desde la línea de comandos con parámetros que puedan controlar el comportamiento, tal como se documenta en [Office Deployment Tool for Click-to-Run](https://docs.microsoft.com/DeployOffice/overview-office-deployment-tool). 
  
**A continuación se muestra un diagrama conceptual de la interfaz COM**

![Diagrama del uso de la interfaz COM en el programa de instalación de Hacer clic y ejecutar de Office.](media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "Diagrama de uso de la interfaz COM en el instalador Office hacer clic y ejecutar")
  
El Aplicaciones Microsoft 365 de hacer clic y ejecutar implementa una interfaz basada en COM, **IUpdateNotify** registrada en CLSID **CLSID_UpdateNotifyObject**.
  
Esta interfaz se puede invocar de la siguiente manera:
  
```cpp
hr = CoCreateInstance(CLSID_UpdateNotifyObject, NULL, CLSCTX_ALL,
       IID_IUpdateNotify, 
      (void **)&p); 
```

La llamada solo se realizará correctamente si el autor de la llamada se ejecuta con privilegios elevados, ya que el programa de instalación Hacer clic y ejecutar debe ejecutarse con privilegios elevados.
  
La **interfaz COM IUpdateNotify** expone tres funciones asincrónicas responsables de validar los comandos y parámetros y programar la ejecución con el servicio de instalación Hacer clic y ejecutar. 
  
```cpp
HRESULT Download([in] LPWSTR pcwszParameters) // Download update content.
HRESULT Apply([in] LPWSTR pcwszParameters) // Apply update content.
HRESULT Cancel() // Cancel the download action.

```

Un método forth, **Status**, se puede usar para obtener información sobre el estado del último comando ejecutado o el estado del comando actualmente en ejecución (es decir, correcto, error, códigos de error detallados).
  
```cpp
HRESULT status([out] _UPDATE_STATUS_REPORT* pUpdateStatusReport) // Get status of current action. 
typedef struct _UPDATE_STATUS_REPORT  
{  
UPDATE_STATUS status;  
UINT error; 
BSTR contentid;  
} UPDATE_STATUS_REPORT;

```

Hay cuatro estados en los que puede estar el servicio de instalación Hacer clic y ejecutar durante su ciclo de vida, durante el cual se puede llamar a los métodos **IUpdateNotify;** Reinicio, inactividad, descarga y aplicación. 
  
**A continuación se muestra el diagrama máquina de estado de interfaz COM**

![Un diagrama de estado de la interfaz COM.](media/a409003e-6876-4ab3-bb4c-cd0c0fed5cbb.png "Diagrama de estado de la interfaz COM")
  
> [!NOTE]
> **Reiniciar:** cuando la máquina está arrancando, hay un período de tiempo en el que el servicio del instalador hacer clic y ejecutar no está disponible. Una llamada correcta al método Status después de un reinicio devolverá eUPDATE_UNKNOWN. 
  
**Inactivo:** Cuando el instalador hacer clic y ejecutar está en estado inactivo, puede llamar a: 
  
- **Aplicar:** instalar contenido descargado previamente.
    
- **Cancel**: Devuelve  `0x800000e` , "Se llamó a un método en un momento inesperado".
    
- **Descargar:** descarga nuevo contenido en el cliente para su instalación posterior.
    
- **Estado:** devuelve el resultado de la última acción completada o un mensaje de error si la acción finalizó en error. Si no hay ninguna acción anterior, **Status** devuelve  `eUPDATE_UNKNOWN` .
    
**Descarga:** Cuando el instalador hacer clic y ejecutar está en estado de descarga, puede llamar a: 
  
- **Apply**: Devuelve un **HRESULT** con el valor , "Se llamó a un método  `0x800000e` en un momento inesperado".
    
- **Cancelar:** detiene la descarga y quita el contenido descargado parcialmente.
    
- **Download**: Devuelve un **HRESULT** con el valor , "Se llamó a un método  `0x800000e` en un momento inesperado". 
    
- **Estado:** devuelve **DOWNLOAD_WIP** para indicar que el trabajo de descarga está en curso. 
    
**Aplicar:** Cuando el instalador hacer clic y ejecutar está en el proceso de instalar contenido de descarga previa: 
  
- **Apply**: Devuelve un **HRESULT** con el valor , "Se llamó a un método  `0x800000e` en un momento inesperado".
    
- **Cancel**: Devuelve  `0x800000e` , la acción Aplicar no se puede cancelar.
    
- **Download**: Devuelve un **HRESULT** con el valor , "Se llamó a un método  `0x800000e` en un momento inesperado". 
    
- **Estado:** devuelve **APPLY_WIP** para indicar que el trabajo de aplicación está en curso. 
    
> [!NOTE]
> Dado que OfficeC2RCOM es un servicio COM+ y se carga dinámicamente, debe llamar a **CoCreateInstance** cada vez que llame a un método en esta clase para asegurarse de obtener el resultado esperado. El servicio COM+ controlará la creación de una nueva instancia si es necesario. Cuando se llama a uno de los métodos por primera vez, COM+ cargará el objeto **IUpdateNotify** y lo ejecutará en una de las dllhost.exe. El nuevo objeto permanecerá activo durante unos 3 minutos en inactividad. Si se realiza una llamada posterior dentro de los tres minutos siguientes a la última llamada, el objeto **IUpdateNotify** permanecerá cargado y no se creará una nueva instancia. Si no se realiza ninguna llamada en tres minutos, se descargará el objeto IUpdateNotify y se creará un nuevo objeto **IUpdateNotify** cuando se haga la siguiente llamada. 
  
## <a name="click-to-run-installer-com-api-reference-guide"></a>Guía de referencia de api com del instalador de hacer clic y ejecutar

En la siguiente documentación de referencia de api:
  
- Los parámetros están en un formato de par clave/valor separados por un espacio.
    
- Los parámetros no distinguen mayúsculas de minúsculas.
    
- Hay una lista [de parámetros con](https://blogs.technet.microsoft.com/odsupport/2014/03/03/the-new-update-now-feature-for-office-2013-click-to-run-for-office365-and-its-associated-command-line-and-switches/) documentación disponible. 
    
- Ahora se incluye el resumen de la interfaz IUpdateNotify2.
    
### <a name="apply"></a>Aplicar

```cpp
HRESULT Apply([in] LPWSTR pcwszParameters) // Apply update content.
```

#### <a name="parameters"></a>Parameters

-  _displaylevel:_ **true** para mostrar el estado de instalación, incluidos los errores, durante el proceso de actualización; **false** para ocultar el estado de instalación, incluidos los errores, durante el proceso de actualización. El valor predeterminado es **false**.
    
-  _forceappshutdown:_ **true** para forzar que Office aplicaciones se apaguen inmediatamente cuando se desencadene **la** acción Aplicar; **false** para producir un error si Office aplicaciones se están ejecutando. El valor predeterminado es **false**. Vea [Comentarios para](#bk_ApplyRemark) obtener más información. 
    
  Si alguna Office se ejecuta cuando **se** desencadena la acción Aplicar, **normalmente** se producirá un error en la acción Aplicar. Pasar  `forceappshutdown=true` al método **Apply** hará que el **servicio OfficeClickToRun** cierre inmediatamente las aplicaciones y aplique la actualización. El usuario puede experimentar la pérdida de datos en este caso. 
    
#### <a name="return-results"></a>Resultados devueltos

|||
|:-----|:-----|
|**S_OK** <br/> |La acción se envió correctamente al servicio Hacer clic y ejecutar para su ejecución.  <br/> |
|**E_ACCESSDENIED** <br/> |El autor de la llamada no se ejecuta con privilegios elevados.  <br/> |
|**E_INVALIDARG** <br/> |Se pasaron parámetros no válidos.  <br/> |
|**E_ILLEGAL_METHOD_CALL** <br/> |La acción no está permitida en este momento. Vea [Comentarios para](#bk_ApplyRemark) obtener más información.  <br/> |

<a name="bk_ApplyRemark"></a>

#### <a name="remarks"></a>Comentarios

- Si alguna Office se ejecuta cuando se desencadena **la** acción Aplicar, se producirá un error **en la acción** Aplicar. Pasar al método Apply hará que el servicio `forceappshutdown=true` **OfficeClickToRun** cierre inmediatamente las aplicaciones Office que se estén ejecutando y apliquen la actualización.  Es posible que el usuario experimente datos, ya que no se le pedirá que guarde los cambios en documentos abiertos. 
    
- Esta acción solo se puede desencadenar cuando el estado COM es uno de los siguientes: 
    
  - **eUPDATE_UNKNOWN**
    
  - **eDOWNLOAD_CANCELLED**
    
  - **eDOWNLOAD_FAILED**
    
  - **eDOWNLOAD_SUCCEEDED**
    
  - **eAPPLY_SUCCEEDED**
    
  - **eAPPLY_FAILED**
    
- Si llama al **método Apply** sin descargar contenido previamente, el método **Apply** se mostrará  **correctamente,** ya que no detectó nada que aplicar y completó correctamente el proceso Aplicar. 
    
### <a name="cancel"></a>Cancelar

```cpp
HRESULT Cancel() // Cancel the download action.
```

#### <a name="return-results"></a>Resultados devueltos

|||
|:-----|:-----|
|S_OK  <br/> |La acción se envió correctamente al servicio Hacer clic y ejecutar para su ejecución.  <br/> |
|E_ILLEGAL_METHOD_CALL  <br/> |La acción no está permitida en este momento. Vea la [sección Comentarios](#bk_CancelRemarks) para obtener más información  <br/> |

<a name="bk_CancelRemarks"></a>

#### <a name="remarks"></a>Comentarios

- Este método solo se puede desencadenar cuando el identificador de estado COM **eDOWNLOAD_WIP**. Intentará cancelar la acción de descarga actual. El estado COM cambiará a **eDOWNLOAD_CANCELLING** y, finalmente, cambiará **a eDOWNLOAD_CANCELED**. El estado COM **devolverá** E_ILLEGAL_METHOD_CALL si se desencadena en cualquier otro momento. 
    
### <a name="download"></a>Descargar

```cpp
HRESULT Download([in] LPWSTR pcwszParameters) // Download update content.
```

#### <a name="parameters"></a>Parameters

-  _displaylevel:_ **true** para mostrar el estado de instalación, incluidos los errores, durante el proceso de actualización; **false** para ocultar el estado de instalación, incluidos los errores, durante el proceso de actualización. El valor predeterminado es **false**.
    
-  _updatebaseurl:_ dirección URL del origen de descarga alternativo.
    
-  _updatetoversion:_ la versión a la que se Office actualizar. Defina este parámetro si desea actualizar a una versión anterior a la que está instalada actualmente.
    
-  _downloadsource:_ CLSID de la implementación personalizada de **IBackgroundCopyManager** (administrador de BITS). 
    
-  _contentid:_ identifica el contenido que se debe descargar desde el servidor de contenido a través del administrador de BITS personalizado. Este valor se pasa a través de la interfaz BITS para su interpretación.
    
#### <a name="return-results"></a>Resultados devueltos

|||
|:-----|:-----|
|**S_OK** <br/> |La acción se envió correctamente al servicio Hacer clic y ejecutar para su ejecución.  <br/> |
|**E_ACCESSDENIED** <br/> |El autor de la llamada no se ejecuta con privilegios elevados.  <br/> |
|**E_INVALIDARG** <br/> |Se pasaron parámetros no válidos.  <br/> |
|**E_ILLEGAL_METHOD_CALL** <br/> |La acción no está permitida en este momento. Vea [Comentarios para](#bk_DownloadRemark) obtener más información.  <br/> |

<a name="bk_DownloadRemark"></a>

#### <a name="remarks"></a>Comentarios

- Debe especificar  _downloadsource_ y  _contentid_ como un par. Si no es así, **el método Download** devolverá un **E_INVALIDARG** error. 
    
- Si _se proporcionan downloadsource_, _contentid_ y _updatebaseurl,_ se omitirá _updatebaseurl._ 
    
- Esta acción solo se puede desencadenar cuando el estado COM es uno de los siguientes: 
    
  - **eUPDATE_UNKNOWN**
    
  - **eDOWNLOAD_CANCELLED**
    
  - **eDOWNLOAD_FAILED**
    
  - **eDOWNLOAD_SUCCEEDED**
    
  - **eAPPLY_SUCCEEDED**
    
  - **eAPPLY_FAILED**
    
- Si llama al **método Apply** sin contenido descargado previamente, el método **Apply** se mostrará  **correctamente,** ya que no detectó nada que aplicar y completó correctamente el proceso Apply. 
    
#### <a name="examples"></a>Ejemplos

- Para descargar el contenido desde el administrador de BITS personalizado: llame a la **función download()** pasando los siguientes parámetros: 
    
  ```cpp
  "downloadsource=CLSIDofBITSInterface contentid=BITSServerContentIdentifier"
  ```

- Para descargar el contenido del Office Content Delivery Network (CDN): llame a la **función download()** sin especificar los parámetros _downloadsource_, _contentid_ o _updatebaseurl._ 
    
- Para descargar el contenido desde una ubicación personalizada: llame a la **función download()** pasando el siguiente parámetro: 
    
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
| _pUpdateStatusReport_ <br/> |Puntero a una UPDATE_STATUS_REPORT estructura.  <br/> |
   
#### <a name="return-results"></a>Resultados devueltos

|||
|:-----|:-----|
|**S_OK** <br/> |El **método Status** siempre devuelve este resultado. Inspeccione la  `UPDATE_STATUS_RESULT` estructura para ver el estado de la acción actual.  <br/> |
   
#### <a name="remarks"></a>Comentarios

- El campo de estado del  `UPDATE_STATUS_REPORT` contiene el estado de la acción actual. Se devuelve uno de los siguientes valores de estado: 
    
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

- Si el último comando produjo un error, el campo de error del contiene  `UPDATE_STATUS_REPORT` información detallada sobre el error. Se devuelven dos tipos de códigos de error del **método Status.** 
    
- Si el error es menor que , el error es uno de los siguientes códigos  `UPDATE_ERROR_CODE::eUNKNOWN` de error predefinidos:
    
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

  Si el código de error devuelto es mayor  `UPDATE_ERROR_CODE::eUNKNOWN` que el **HRESULT** de una llamada de función con error. Para extraer la resta HRESULT  `UPDATE_ERROR_CODE::eUNKNOWN` del valor devuelto en el campo de error de  `UPDATE_STATUS_REPORT` .
    
  La lista completa de valores de estado y error se puede ver inspeccionando la biblioteca de tipos **IUpdateNotify** incrustada en OfficeC2RCom.dll. 
    
- El campo contentid se usa para las llamadas a **Estado** después de iniciar **la** descarga y devuelve el contentid que se pasó a la **llamada Descargar.** Es un procedimiento recomendado inicializar este campo en **null** antes de llamar al **método Status** y, a continuación, comprobar el valor después de que se haya devuelto **Status.** Si el valor sigue siendo **null**, significa que no hay contentid que devolver. Si el valor no es **nulo,** debe liberarlo con una llamada a **SysFreeString()**. Este es un fragmento de código de cómo llamar a **Estado** después de **descargar**.
    
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

### <a name="summary-of-iupdatenotify2-interface"></a>Resumen de la interfaz IUpdateNotify2

Desde la versión [16.0.8208.6352] hemos agregado una nueva interfaz **IUpdateNotify2.** 
  
- CLSID_UpdateNotifyObject2, {52C2F9C2-F1AC-4021-BF50-756A5FA8DDFE}
    
- Esta interfaz también hospedaba la interfaz IUpdateNotify original para proporcionar compatibilidad con versiones anteriores. Lo que significa que si usa esta interfaz, tendrá acceso a todos los métodos proporcionados en la interfaz **UpdateNotifyObject.** 
    
- Nuevos métodos agregados a IUpdateNotify2:
    
  - **HRESULT** GetBlockingApps([out] BSTR \* AppsList). Obtener la lista de aplicaciones de bloqueo de actualizaciones. Esta llamada devolverá la ejecución Office aplicaciones que impedirán que el proceso de actualización continuara. 
    
  - **HRESULT** GetOfficeDeploymentData([in] int dataType, [in] **LPCWSTR** pcwszName, [out] BSTR * OfficeData). Obtenga Office de implementación. 
    
- Si desea usar los nuevos métodos, debe asegurarse de:
    
  - La versión C2R es más reciente que la compilación anterior ( \> = Compilación de bifurcación de junio).
    
  - Use UpdateNotifyObject2, en lugar **de UpdateNotifyObject para** llamar **a CoCreateInstance**.
    
Si no usa ninguno de los nuevos métodos, no necesita cambiar nada. Todos los métodos existentes funcionarán exactamente igual que antes.
  
## <a name="implementing-the-bits-interface"></a>Implementación de la interfaz BITS

El [Servicio de transferencia inteligente en segundo](https://docs.microsoft.com/windows/win32/bits/background-intelligent-transfer-service-portal) plano (BITS) es un servicio proporcionado por Microsoft para transferir archivos entre un cliente y un servidor. BITS es uno de los canales que Office instalador hacer clic y ejecutar puede usar para descargar contenido. De forma predeterminada, el instalador Aplicaciones Microsoft 365 hacer clic y ejecutar usa la implementación integrada de BITS de Windows para descargar el contenido de la CDN. 
  
Al proporcionar una implementación de BITS personalizada al método **download()** de la interfaz **IUpdateNotify,** el software de administración puede controlar dónde y cómo descarga el contenido el cliente. Una interfaz BITS personalizada es útil al proporcionar un canal de distribución de contenido personalizado que no sea los canales integrados Hacer clic y ejecutar, como el CDN, los servidores IIS o los recursos compartidos de archivos. 
  
El requisito mínimo para que una interfaz BITS personalizada funcione con Office C2R es:
  
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

- Para las  `Addfile` funciones  `AddFileWithRanges` y, la dirección URL remota tiene el siguiente formato: 
    
  ```cpp
  cmbits://<contentid>/<relative path to target file>
  ```

  - cmbits está codificado de forma dura y significa BITS personalizados.
    
  -  _\<contentid\>_ es el _parámetro contentid_ del **método Download().** 
    
  -  _\<relative path to target file\>_ proporciona la ubicación y el nombre de archivo del archivo que se debe descargar. 
    
    Por ejemplo, si ha proporcionado un _contentid_ del método Download() y Office C2R desea descargar el archivo cab de versión, como file, llamará `f732af58-5d86-4299-abe9-7595c35136ef` a  `v32.cab` **AddFile()** con lo `RemoteUrl` siguiente:
    
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
## <a name="automating-content-staging"></a>Automatizar el almacenamiento provisional de contenido

Los administradores de TI pueden elegir que los clientes de escritorio estén habilitados para recibir automáticamente actualizaciones cuando estén disponibles directamente desde el CDN o pueden elegir controlar la implementación de actualizaciones disponibles desde los canales de actualización mediante la herramienta de implementación de Office o Microsoft Endpoint Configuration Manager.
  
El servicio admite la capacidad de las herramientas de administración para reconocer y automatizar la descarga del contenido cuando las actualizaciones están disponibles.
  
**La siguiente imagen es una introducción a la descarga de una imagen personalizada**

![Diagrama del uso de la interfaz COM en el programa de instalación de Hacer clic y ejecutar de Office.](media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "Diagrama de uso de la interfaz COM en el instalador Office hacer clic y ejecutar")
  
### <a name="overview-of-downloading-a-custom-image"></a>Información general sobre la descarga de una imagen personalizada
  
En el diagrama anterior, verá que una nueva imagen Aplicaciones Microsoft 365 está disponible en el CDN. Junto con la imagen Aplicaciones Microsoft 365, hay disponible una API que tiene la información necesaria para permitir que el software de administración cree directamente imágenes personalizadas que reemplacen la necesidad de usar la herramienta de implementación de Office.

Una empresa configura su WSUS para sincronizar las Aplicaciones Microsoft 365 actualizaciones. Estas actualizaciones no contienen la carga real de la imagen, pero permiten que el software de administración reconozca cuándo hay contenido nuevo disponible. A continuación, el software de administración puede leer los metadatos Aplicaciones Microsoft 365 update para comprender a qué versión de Office se aplica la actualización.

Si la actualización es aplicable, el software de administración puede usar el contenido de CDN y la lista de archivos para crear la imagen personalizada y almacenarla en la ubicación del recurso compartido de archivos que está configurada para usar.
  
### <a name="using-the-microsoft-365-apps-file-list-api"></a>Uso de la API Aplicaciones Microsoft 365 lista de archivos

La API Aplicaciones Microsoft 365 lista de archivos se usa para recuperar los nombres de los archivos necesarios para una actualización Aplicaciones Microsoft 365 archivo.

Solicitud HTTP

GET https://config.office.com/api/filelist

No proporcione un cuerpo de solicitud para este método.

No se requieren permisos para llamar a esta API.

Parámetros de consulta opcionales

|**Nombre**|**Descripción**|
|:-----|:-----|
| channel <br/>| Especifica el nombre del canal  <br/> Opcional: valor predeterminado en 'SemiAnnual' <br/> Valores admitidos https://docs.microsoft.com/DeployOffice/office-deployment-tool-configuration-options#channel-attribute-part-of-add-element |
| version <br/>| Especifica la versión de actualización <br/> Opcional: el valor predeterminado es la versión más reciente disponible para el canal especificado |
| arco <br/>| Especifica la arquitectura de cliente <br/> Opcional: el valor predeterminado es 'x64' <br/> Valores admitidos: x64, x86 |
| lid <br/>| Especifica los archivos de idioma que se incluirán <br/> Opcional: el valor predeterminado es none <br/> Para especificar varios idiomas, incluya un parámetro de consulta de tapa para cada idioma <br/> Use el formato de identificador de idioma, por ejemplo. 'en-us', 'fr-fr' |
| alllanguages <br/>| Especifica para incluir todos los archivos de idioma <br/> Opcional: el valor predeterminado es false |

Respuesta HTTP

Si se realiza correctamente, este método devuelve un código de respuesta 200 Aceptar y una colección de objetos de archivo en el cuerpo de la respuesta.

Para crear una imagen, siga estos pasos:
1.  Llama a la API y proporciona los parámetros de consulta adecuados para el canal, la versión y la arquitectura de la actualización que te interesa.
Nota: Los objetos de archivo con el atributo "lcid": "0" son archivos sin idioma y deben incluirse en la imagen.
2.  Construya una imagen local del CDN iterando por los objetos de archivo y copiando los archivos de CDN, al mismo tiempo que crea la estructura de carpetas especificada por el atributo "relativePath" definido para cada uno de los objetos de archivo.

En el siguiente ejemplo se recupera la lista de archivos del canal actual y la versión 16.0.4229.1004 para 64 bits e incluye los archivos en francés e inglés:

```http
Get https://config.office.com/api/filelist?Channel=Current&Version=16.0.4229.1004&Arch=x64&Lid=fr-fr&Lid=en-US
```

### <a name="hash-verification-of-dat-files"></a>Comprobación hash de archivos .dat

Las herramientas de creación de imágenes pueden comprobar la integridad de los archivos .dat descargados comparando un valor hash calculado con el valor hash proporcionado asociado a cada uno de los archivos .dat. A continuación se muestra un ejemplo de un objeto de archivo que especifica valores hashLocation y hashAlgorithm:
  
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

- El **atributo hashLocation** especifica la ubicación de ruta de acceso relativa del .cab que contiene el valor hash. Construya la ubicación del archivo hash concatenando dirección URL + relativePath + hashLocation. En el siguiente ejemplo, la stream.x64.bg-bg.hash sería: 
    
  ```http
  https://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/16.0.4229.1004/s641026.cab/stream.x64.bg-bg.hash 
  ```

- El **atributo hashAlgorithm** especifica qué algoritmo hash se usó. 
    
  Para validar la integridad del archivo stream.x64.bg-bg.dat, abra el archivo stream.x64.bg-bg.hash y lea el valor HASH que es la primera línea de texto del archivo hash. Compare esto con el valor hash calculado (mediante el algoritmo hash especificado) para comprobar la integridad del archivo .dat descargado.
    
  En el ejemplo siguiente se muestra C# código para leer el hash.
    
  ```cs
    string[] readHashes = System.IO.File.ReadAllLines(tmpFile, Encoding.Unicode);
    string readHash = readHashes.First();
  ```

### <a name="microsoft-365-apps-updates"></a>Aplicaciones Microsoft 365 Actualizaciones

Todas Aplicaciones Microsoft 365 actualizaciones se publican en el [Catálogo de Microsoft Update](https://www.catalog.update.microsoft.com/Search.aspx?q=office+365+client).
  
Aplicaciones Microsoft 365 Las actualizaciones permiten que el software de administración trate Aplicaciones Microsoft 365 actualizaciones de una manera muy similar a cualquier otra actualización de WU con una excepción; las actualizaciones de cliente no contienen una carga real. Las actualizaciones Aplicaciones Microsoft 365 no deben instalarse en ningún cliente, sino que se deben usar para desencadenar los flujos de trabajo con el software de administración que reemplaza el comando de instalación por el mecanismo de instalación basado en COM mostrado anteriormente.

**En la siguiente figura se muestra un diagrama del flujo Office 365 de actualización de cliente.**

![Diagrama de flujo de trabajo para las actualizaciones de cliente de O365PP.](media/bc8092b0-62b8-402c-a5c0-04d55cca01d4.png "Diagrama de flujo de trabajo para actualizaciones de cliente de O365PP")
  
Cada Aplicaciones Microsoft 365 que se publica incluye metadatos sobre la actualización. Estos metadatos incluyen un parámetro denominado MoreInfoUrl que se puede usar para derivar la llamada api a la API de lista de archivos para esa actualización específica.

En el siguiente ejemplo, la API de lista de archivos está incrustada en MoreInfoURL y comienza por "ServicePath="

http://go.microsoft.com/fwlink/?LinkId=626090&Ver=16.0.12527.21104&Branch=Insiders&Arch=64&XMLVer=1.6&xmlPath=http://officecdn.microsoft.com/pr/wsus/ofl.cab&xmlFile=O365Client_64bit.xml& ServicePath=https://config.office.com/api/filelist?Channel=Insiders&Version=16.0.12527.21104&Arch=64&AllLanguages=True
  
### <a name="additional-metadata-for-automating-content-staging"></a>Metadatos adicionales para automatizar el almacenamiento provisional de contenido

**API de historial de versiones**
  
La API Aplicaciones Microsoft 365 historial de versiones se usa para recuperar los detalles de cada una de las actualizaciones publicadas en el CDN junto con los nombres de canal y otros atributos de canal.

Solicitud HTTP

```http
GET https://config.office.com/api/filelist/channels 
```

No proporcione un cuerpo de solicitud para este método.

No se requieren permisos para llamar a esta API.

Respuesta HTTP

Si se realiza correctamente, este método devuelve un código de respuesta 200 Aceptar y una colección de objetos de archivo en el cuerpo de la respuesta.

**API de SKU**
  
La API de SKU devuelve información que resulta útil para determinar qué productos están disponibles para la implementación y el mantenimiento desde el Office CDN junto con varias opciones para cada uno.

Solicitud HTTP

```http
GET https://config.office.com/api/filelist/skus 
```

No proporcione un cuerpo de solicitud para este método.

No se requieren permisos para llamar a esta API.

Respuesta HTTP

Si se realiza correctamente, este método devuelve un código de respuesta 200 Aceptar y una colección de objetos de archivo en el cuerpo de la respuesta.
