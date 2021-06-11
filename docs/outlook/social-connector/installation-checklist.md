---
title: Lista de comprobación de la instalación
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9dfb9b6d-2fb4-45bf-a12f-bd10a799ce29
description: En este tema se describen los requisitos previos para instalar correctamente un proveedor de Outlook Social Connector (OSC) y la instalación comprueba que el instalador del proveedor debe completarse para funcionar correctamente.
ms.openlocfilehash: 8fec8523e57ad2678d02a0c5cbc1ad57340e5267
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286346"
---
# <a name="installation-checklist"></a>Lista de comprobación de la instalación

En este tema se describen los requisitos previos para instalar correctamente un proveedor de Outlook Social Connector (OSC) y la instalación comprueba que el instalador del proveedor debe completarse para funcionar correctamente.
  
## <a name="installation-overview"></a>Introducción a la instalación

Los usuarios deben instalar proveedores de OSC solo si hay una versión compatible de Outlook y el OSC está instalado y habilitado en el equipo cliente. Las versiones compatibles de Outlook son Office Outlook 2003, Office Outlook 2007, Outlook 2010 y Outlook 2013 (instalados en el equipo cliente o, en el caso de Outlook 2010 y Outlook 2013, entregados por Hacer clic y ejecutar en el equipo cliente). Para garantizar una instalación correcta, el instalador del proveedor debe hacer lo siguiente:
  
- Compruebe si hay una versión compatible de Outlook está presente.
    
- Compruebe si el OSC está instalado.
    
> [!NOTE]
> Hacer clic y ejecutar es un entorno virtual en el que Outlook 2010 (32 bits) o Outlook 2013 (32 bits). Para Outlook 2013, compruebe si la clave VirtualOutlook existe en HKEY_LOCAL_MACHINE\Software\Microsoft\Office\15.0\Common\InstallRoot\Virtual\VirtualOutlook del Windows registro. Para obtener más información acerca de la entrega de Outlook como un producto hacer clic y ejecutar en un equipo cliente, vea How [to Verify if Outlook is Available on a Computer as a Click-to-Run Product](https://blogs.msdn.com/b/officedevdocs/archive/2010/03/09/how-to-verify-if-outlook-is-available-on-a-computer-as-a-click-to-run-product.aspx). 
  
Sin embargo, el usuario debe asegurarse de que el OSC está habilitado antes de instalar el proveedor.
  
Terceros, incluidos los proveedores de OSC, no pueden redistribuir el OSC. Sin embargo, si el OSC no está instalado, el instalador del proveedor puede usar los vínculos g adecuados para instalar el OSC en el equipo cliente. Un vínculo g es una dirección URL especialmente construida en la que se reenvía un usuario a una página web https://g.live.com correspondiente para descargar el OSC. Un vínculo g de OSC tiene el formato https://g.live.com/0CR _LCID_ /  _Glink_, donde _LCID_ y _Glink_ especifican la configuración regional, la versión y la bitness de Outlook en el equipo cliente. Cada vínculo g apunta a un archivo ejecutable y es específico de los valores _LCID_ y _Glink especificados._ 
  
Por ejemplo, el vínculo g para instalar la versión más reciente del OSC para Outlook 2003 o Outlook 2007 para LCID 1033 (inglés estadounidense) es el siguiente:
  
https://g.live.com/0CR1033/80
  
Para obtener información detallada acerca de los valores _de Glink_ para diferentes versiones y bits de Outlook y _valores LCID_ para configuraciones regionales admitidas, vea #7 en la sección [Lista](#olosc_InstallationOverview_InstallationChecklist) de comprobación de instalación siguiente. 

<a name="olosc_InstallationOverview_InstallationChecklist"> </a>

## <a name="installation-checklist"></a>Lista de comprobación de la instalación

El paquete de instalación del proveedor debe realizar una serie de comprobaciones de instalación, como se muestra en la figura 1, para asegurarse de que el proveedor se instala correctamente.
  
**Figura 1. Lógica de instalación del proveedor**

![Lista de comprobación de la instalación](media/odc_ol14_ta_OSC_Fig07.gif)
  
El siguiente procedimiento describe las comprobaciones de instalación descritas en la figura 1.
  
1. Como requisito previo, detecte si Outlook está instalado o presente, y si está instalado o presente, determine si la versión de Outlook es compatible con el OSC. Para obtener más información acerca de la detección de la versión instalada de Outlook, vea [Comprobar la versión de Outlook](https://msdn.microsoft.com/library/672fc380-a29b-4e99-9211-949fd5065723%28Office.15%29.aspx).
    
   - Si la versión instalada de Outlook es anterior a Outlook 2003, el procedimiento de instalación del proveedor no se puede completar. Informe al usuario para obtener una versión compatible de Outlook y el OSC antes de continuar con la instalación del proveedor de OSC.
    
   - Si Outlook no está instalado, continúe con el paso 2.
    
   - Si Outlook 2003 o Outlook 2007 está instalado, vaya al paso 3. 
    
   - Si Outlook 2010 o Outlook 2013 está instalado, vaya al paso 4.
    
2. **Continúe con este paso si Outlook no está instalado en el equipo cliente:**
    
   1. Compruebe si el OSC está instalado como un componente predeterminado de una instalación hacer clic y ejecutar de Outlook 2010 o Outlook 2013. Examine la `VirtualOutlook` clave en la siguiente ubicación en el Windows registro: 
      
      - Para Outlook 2010,`HKEY_LOCAL_MACHINE\Software\Microsoft\Office\14.0\Common\InstallRoot\Virtual\VirtualOutlook`
      
      - Para Outlook Social Connector 2013,`HKEY_LOCAL_MACHINE\Software\Microsoft\Office\15.0\Common\InstallRoot\Virtual\VirtualOutlook`
      
      La clave es un REG_SZ que contiene la etiqueta de configuración regional, como  `VirtualOutlook` "en-us&quot;, del producto instalado. 
      
   2. Si la clave no existe, Outlook está presente en el equipo cliente y el procedimiento de instalación `VirtualOutlook` del proveedor no se puede completar. Informe al usuario para obtener una versión compatible de Outlook y el OSC antes de continuar con la instalación del proveedor de OSC. 
      
   3. Si la clave existe, Outlook la entregó `VirtualOutlook` Click-to-Run en el equipo cliente. Para comprobar la versión instalada de la biblioteca de tipos de OSC, examine la clave en la siguiente ubicación en el `OSCVersion` Windows registro: 
      
      `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\OSCVersion`
      
      El valor de es una cadena que especifica el número de versión de biblioteca de tipos de  `OSCVersion` Socialprovider.dll (por ejemplo, &quot;1.0&quot;, &quot;1.1&quot; o &quot;15"). 
      
   4. Si  `OSCVersion` es "1.0", "1.1" o "15", se instala una versión adecuada de OSC. Continúe con el paso 6 para buscar la configuración regional Outlook interfaz de usuario actual para prepararse para instalar la versión más reciente del OSC. 
      
   5. De lo  `OSCVersion` contrario, no contiene un valor esperado. Continúe con el paso 6 para buscar la configuración regional Outlook interfaz de usuario actual para preparar la instalación de una versión adecuada del sistema operativo. 
    
3. **Continúe con este paso si Outlook 2003 o Outlook 2007 está instalado en el equipo cliente:**
    
   1. Compruebe si el OSC está instalado escribiendo una acción personalizada del instalador para comprobar la existencia del siguiente identificador de componente cualificado:
      
      `{A3B82DA3-8AD9-4935-AEA8-54B754459483}`
      
      El identificador de componente cualificado es un GUID que proporciona un método de direccionamiento indirecto de un solo nivel, similar a un puntero. Para obtener más información sobre Windows Installer, consulte [Roadmap to Windows Installer Documentation](https://docs.microsoft.com/windows/desktop/msi/roadmap-to-windows-installer-documentation).
      
   2. Si existe el componente cualificado especificado, se instala una versión del OSC. Continúe con el paso 5 para buscar la configuración regional Outlook interfaz de usuario actual para prepararse para instalar la versión más reciente del OSC.
      
   3. De lo contrario, el OSC no está instalado. Continúe con el paso 6 para buscar la configuración regional Outlook interfaz de usuario actual para preparar la instalación de una versión adecuada del sistema operativo.
      
4. **Continúe con este paso si Outlook 2010 o Outlook 2013 está instalado en el equipo cliente:**
    
   1. Determine la bitness de la versión instalada de Outlook mediante el examen de la clave en la siguiente ubicación en el `Bitness` Windows registro: 
      
      - Para Outlook 2010, vea`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\14.0\Outlook`
      
      - Para Outlook 2013, vea`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Outlook`
      
      La clave es "x86" para los Outlook de 32 bits o "x64" para los Outlook `Bitness` de 64 bits. 
      
   2. Si su proveedor es un proveedor administrado y ha compilado el componente de proveedor que especifica la plataforma de destino como Cualquier **CPU,** continúe con el paso 6 para buscar la configuración regional de la interfaz de usuario de Outlook actual para prepararse para instalar la versión más reciente del OSC. El proveedor trabajará en versiones de 32 y 64 bits del OSC.
      
   3. Si el proveedor es un componente COM nativo, examine la bitness de la versión instalada de Outlook:
      
      - Si la versión instalada de Outlook es de 32 bits, el procedimiento de instalación tendrá que instalar un proveedor de 32 bits (en el paso 8), después de asegurarse de que se instala un OSC adecuado.
      
      - De lo contrario, la versión instalada de Outlook es de 64 bits y el procedimiento de instalación tendrá que instalar un proveedor de 64 bits (en el paso 8), después de asegurarse de que se instala un OSC adecuado. 
      
   4. Continúe con el paso 6 para buscar la configuración regional Outlook interfaz de usuario actual para prepararse para instalar una versión adecuada del OSC.
    
5. **Continúe con este paso si Outlook 2003 o Outlook 2007** está instalado y el OSC está instalado en el equipo cliente: Compruebe la configuración Outlook configuración regional de la interfaz de usuario mediante el examen de la clave en la siguiente ubicación en `OSCLcid` el Windows usuario: 
    
   `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\OSCLcid`
    
   La clave es un valor DWORD que especifica la etiqueta de configuración regional del Grupo de tareas de ingeniería de `OSCLcid` Internet (IETF) (definida por [[RFC4646]](https://www.ietf.org/rfc/rfc4646.txt) y [[RFC4647]](https://www.ietf.org/rfc/rfc4647.txt)), que representa la configuración regional de la interfaz de usuario de Outlook actual. Continúe con el paso 7 para instalar el último OSC en el equipo cliente.
    
6. **Continúe con este paso si Outlook 2003 o Outlook 2007 está instalado o Outlook 2010 o Outlook 2013 está presente, pero el último OSC no está necesariamente instalado en el equipo cliente:**
    
   Use el **objeto LanguageSettings** para determinar el LCID de la configuración regional Outlook interfaz de usuario. El siguiente Visual Basic de código de Scripting Edition (VBScript) muestra cómo obtener el LCID de la configuración regional Outlook interfaz de usuario. 
    
   ```vb
    Function GetOutlookUI_LCID()
        ' Declare variables.
        Dim msoLanguageIDUI, olApp
        msoLanguageIDUI = 2
        Set olApp = CreateObject("Outlook.Application")
        ' Return Outlook UI LCID.
        GetOutlookUI_LCID = olApp.LanguageSettings.LanguageID(msoLanguageIDUI)
    End Function
   ```

7. **Continúe con este paso si el instalador tiene el LCID de la versión instalada de Outlook, pero el último OSC no está necesariamente instalado en el equipo cliente:**
    
   Encadena un vínculo g en el paquete de instalación para garantizar que la versión más reciente del OSC esté instalada en el equipo cliente. El formato de vínculo g es el siguiente:
    
   https://g.live.com/0CR_LCID_ /  _Glink_
    
   Consulte la tabla 1 siguiente para los valores _LCID_ admitidos y la tabla 2 para los _valores de Glink admitidos._ Por ejemplo, el vínculo g para instalar la versión más reciente del OSC de 32 bits para Outlook Social Connector 2013 de 32 bits (inglés de EE.UU.) es el siguiente: 
    
   https://g.live.com/0CR1033/82
    
8. Instale el proveedor. El procedimiento de instalación del proveedor debe registrar el identificador de programación (ProgID) en la ubicación Windows registro. Para obtener más información, vea [Registering a Provider](registering-a-provider.md). Además, asegúrese de que la bitness del proveedor que se va a instalar sea la misma que la bitness de la versión de Outlook presente en el equipo cliente. Por ejemplo, instale un proveedor de 32 bits si Outlook 2013 de 32 bits está presente y un proveedor de 64 bits si está instalado Outlook 64 bits de 2013. Por Outlook 2003 o 2007, solo se aplica la versión de 32 bits del proveedor. 
    
**Tabla 1: Configuración regional admitida y valores LCID correspondientes en hexadecimal para el OSC**
  
|**Locale**|**LCID**|
|:-----|:-----|
|ar-sa  <br/> |1025  <br/> |
|bg-bg  <br/> |1026  <br/> |
|ca-es  <br/> |1027  <br/> |
|cs-cz  <br/> |1029  <br/> |
|da-dk  <br/> |1030  <br/> |
|de-de  <br/> |1031  <br/> |
|el-gr  <br/> |1032  <br/> |
|en-us  <br/> |1033  <br/> |
|es-es  <br/> |3082  <br/> |
|et-ee  <br/> |1061  <br/> |
|eu-es  <br/> |1069  <br/> |
|fi-fi  <br/> |1035  <br/> |
|fr-fr  <br/> |1036  <br/> |
|gl-es  <br/> |1110  <br/> |
|he-il  <br/> |1037  <br/> |
|hi-in  <br/> |1081  <br/> |
|hr-hr  <br/> |1050  <br/> |
|hu-hu  <br/> |1038  <br/> |
|it-it  <br/> |1040  <br/> |
|ja-jp  <br/> |1041  <br/> |
|kk-kz  <br/> |1087  <br/> |
|ko-kr  <br/> |1042  <br/> |
|lt-lt  <br/> |1063  <br/> |
|lv-lv  <br/> |1062  <br/> |
|nb-no  <br/> |1044  <br/> |
|nl-nl  <br/> |1043  <br/> |
|pl-pl  <br/> |1045  <br/> |
|pt-br  <br/> |1046  <br/> |
|pt-pt  <br/> |2070  <br/> |
|ro-ro  <br/> |1048  <br/> |
|ru-ru  <br/> |1049  <br/> |
|sk-sk  <br/> |1051  <br/> |
|sl-si  <br/> |1060  <br/> |
|sr-cyrl-cs  <br/> |3098  <br/> |
|sr-latn-cs  <br/> |2074  <br/> |
|sv-se  <br/> |1053  <br/> |
|th-th  <br/> |1054  <br/> |
|tr-tr  <br/> |1055  <br/> |
|uk-ua  <br/> |1058  <br/> |
|zh-cn  <br/> |2052  <br/> |
|zh-tw  <br/> |1028  <br/> |
   
**Tabla 2: Valores de Glink admitidos para el OSC**
  
|**Valor de Glink**|**Función**|
|:-----|:-----|
|80  <br/> |Instala la versión más reciente de OSC para Outlook 2003 o Outlook 2007.  <br/> |
|82  <br/> |Instala la última revisión de OSC de 32 bits para Outlook 2007, Outlook 2010 o Outlook Social Connector 2013.  <br/> |
|83  <br/> |Instala la revisión más reciente de OSC de 64 bits para Outlook 2010 o Outlook Social Connector 2013.  <br/> |
   
## <a name="see-also"></a>Vea también

- [Registro de un proveedor](registering-a-provider.md) 
- [Pasos rápidos para aprender a desarrollar un proveedor](quick-steps-for-learning-to-develop-a-provider.md)
- [Implementación de un proveedor](deploying-a-provider.md)

