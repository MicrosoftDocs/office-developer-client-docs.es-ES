---
title: IMAPIFormContainerInstallForm
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormContainer.InstallForm
api_type:
- COM
ms.assetid: b39ca52c-4dbe-41c0-9e1b-3998a9dc9742
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: fd7bc8f051e9584fc63f22bdbaf9696c2e4d15a3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580939"
---
# <a name="imapiformcontainerinstallform"></a>IMAPIFormContainer::InstallForm

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Instala un formulario en una biblioteca de formularios.
  
```cpp
HRESULT InstallForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPCSTR szCfgPathName
);
```

## <a name="parameters"></a>Parámetros

 _ulUIParam_
  
> [entrada] Identificador de la ventana principal de los cuadros de diálogo o windows que muestra este método. El parámetro _ulUIParam_ se omite a menos que la aplicación cliente establece la marca MAPI_DIALOG en el parámetro _ulFlags indicado_ . El parámetro _ulUIParam_ puede ser NULL si no se pasa también MAPI_DIALOG. 
    
 _ulFlags_
  
> [entrada] Una máscara de bits de indicadores que controla la instalación del formulario. Se pueden establecer los siguientes indicadores:
    
MAPI_DIALOG 
  
> Muestra un cuadro de diálogo para proporcionar información de progreso o solicite al usuario para obtener más información. Si no se establece este marcador, no se muestra ningún cuadro de diálogo.
    
MAPI_UNICODE 
  
> Las cadenas que se pasan en están en formato Unicode. Si no está establecido el indicador MAPI_UNICODE., las cadenas están en formato ANSI.
    
MAPIFORM_INSTALL_OVERWRITEONCONFLICT 
  
> Si otro formulario ya existe que controla la clase de mensaje se controla mediante este formulario, reemplazar el formulario existente con éste. Este indicador se omite si la marca MAPI_DIALOG también está presente. 
    
 _szCfgPathName_
  
> [entrada] La ruta de acceso al archivo de configuración del formulario.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
MAPI_E_EXTENDED_ERROR 
  
> Se ha producido un error en la implementación. Para obtener la estructura [MAPIERROR](mapierror.md) que está asociada con el error, llame al método [IMAPIFormContainer::GetLastError](imapiformcontainer-getlasterror.md) . 
    
MAPI_E_USER_CANCEL 
  
> El usuario canceló la instalación del formulario, normalmente haciendo clic en el botón **Cancelar** en un cuadro de diálogo. 
    
## <a name="notes-to-implementers"></a>Notas a los implementadores

Proveedores de biblioteca de formulario deben rellenar una estructura **MAPIERROR** y devolver MAPI_E_EXTENDED_ERROR si se produce alguna de las condiciones siguientes: 
  
- No se encontró el archivo de configuración.
    
- El archivo de configuración no es legible.
    
- El archivo de configuración no es válido.
    
## <a name="notes-to-callers"></a>Notas para los llamadores

Las aplicaciones cliente de llaman al método **IMAPIFormContainer::InstallForm** para instalar un formulario en un contenedor de forma específicos. El parámetro _szCfgPathName_ debe contener la ruta de acceso de un archivo de configuración de formulario (es decir, un archivo con la extensión .cfg que describe el formulario y su implementación). Las marcas en el parámetro _ulFlags_ especifican lo siguiente: 
  
- Si se establece la marca MAPI_DIALOG, se muestra una interfaz de usuario, permitiendo al usuario que está instalando el formulario para especificar detalles de la instalación.
    
- Si se establece la marca MAPIFORM_INSTALL_OVERWRITEONCONFLICT, se reemplaza cualquier formulario anterior para la misma clase de mensaje con el formulario que se va a instalar. De lo contrario, la instalación de formulario se combina con la descripción del formulario actual, si lo hay.
    
- Si se establece MAPI_DIALOG, MAPIFORM_INSTALL_OVERWRITEONCONFLICT se omite.
    
- La ausencia de MAPIFORM_INSTALL_OVERWRITEONCONFLICT en el indicador establece significa que se va a realizar una combinación. Se instalarán nuevas plataformas en el archivo .cfg que no están actualmente presentes en la descripción del formulario y no se producirá ningún otro cambio.
    
- Si se establece el indicador MAPI_UNICODE., la ruta de acceso del archivo de configuración de formulario es una cadena Unicode. 
    
Los clientes deben llamar [IMAPIFormContainer::GetLastError](imapiformcontainer-getlasterror.md) si **InstallForm** devuelve MAPI_E_EXTENDED_ERROR, y se deben proteger la estructura [MAPIERROR](mapierror.md) devuelta para determinar la condición que provocó el error. 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**File**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|FormContainerDlg.cpp  <br/> |CFormContainerDlg::OnInstallForm  <br/> |MFCMAPI usa el método **IMAPIFormContainer::InstallForm** para instalar un formulario en un contenedor de formulario.  <br/> |
   
## <a name="see-also"></a>Vea también



[MAPIERROR](mapierror.md)
  
[IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

