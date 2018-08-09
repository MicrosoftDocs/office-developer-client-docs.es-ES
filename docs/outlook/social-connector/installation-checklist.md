---
title: Lista de comprobación de la instalación
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9dfb9b6d-2fb4-45bf-a12f-bd10a799ce29
description: En este tema se describe los requisitos previos para instalar correctamente un proveedor de Outlook Social Connector (OSC) y la instalación comprueba que el instalador de proveedor se debe completar para que funcione correctamente.
ms.openlocfilehash: cb8ed24db28c3b0e945c4db4b2daa4a2470d7dd5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821103"
---
# <a name="installation-checklist"></a>Lista de comprobación de la instalación

En este tema se describe los requisitos previos para instalar correctamente un proveedor de Outlook Social Connector (OSC) y la instalación comprueba que el instalador de proveedor se debe completar para que funcione correctamente.
  
## <a name="installation-overview"></a>Introducción a la instalación

Los usuarios deben instalar a proveedores de OSC sólo si está presente una versión compatible de Outlook y el OSC está instalado y habilitado en el equipo cliente. Versiones compatibles de Outlook son Office Outlook 2003, Office Outlook 2007, Outlook 2010 y Outlook 2013 (instalado en el equipo cliente o, en el caso de Outlook 2010 y Outlook 2013, entregado por Click-to-Run en el equipo cliente). Para garantizar una instalación correcta, el instalador de proveedor debe hacer lo siguiente:
  
- Compruebe si existe una versión compatible de Outlook.
    
- Compruebe si está instalado el OSC.
    
> [!NOTE]
> Click-to-Run es un entorno virtual en el que puede ejecutar Outlook 2010 (32 bits) o Outlook 2013 (32 bits). Para Outlook 2013, compruebe si existe la clave de VirtualOutlook en HKEY_LOCAL_MACHINE\Software\Microsoft\Office\15.0\Common\InstallRoot\Virtual\VirtualOutlook del registro de Windows. Para obtener más información acerca de la oferta de Outlook como un producto de Click-to-Run en un equipo cliente, consulte [cómo comprobar si Outlook está disponible en un equipo como un producto de Click-to-Run](http://blogs.msdn.com/b/officedevdocs/archive/2010/03/09/how-to-verify-if-outlook-is-available-on-a-computer-as-a-click-to-run-product.aspx). 
  
Sin embargo, tiene el usuario, para asegurarse de que esté habilitado el OSC antes de instalar al proveedor.
  
Terceros, incluidos los proveedores OSC, no se puede redistribuir el OSC. Sin embargo, si no está instalado el OSC, el instalador de proveedor puede usar vínculos de g adecuados para instalar el OSC en el equipo cliente. Un vínculo de g es una dirección URL construida especialmente en http://g.live.com que reenvía a descargar el OSC un usuario a una página Web correspondiente. Un vínculo de g OSC tiene el formato http://g.live.com/0CR _LCID_/ _Glink_, donde _LCID_ y _Glink_ especifican la configuración regional, la versión y el valor de bits de Outlook en el equipo cliente. Cada g-vínculo apunta a un archivo ejecutable y es específico de los valores _LCID_ y _Glink_ especificados. 
  
Por ejemplo, el vínculo g para instalar la versión más reciente de la OSC para Outlook 2003 u Outlook 2007 para el LCID 1033 (inglés) es como sigue:
  
http://g.live.com/0CR1033/80
  
Para obtener información detallada acerca de los valores de _Glink_ para las diferentes versiones y el valor de bits de Outlook y los valores _LCID_ para las configuraciones regionales admitidas, vea #7 en la sección [Lista de comprobación de instalación](#olosc_InstallationOverview_InstallationChecklist) . 

<a name="olosc_InstallationOverview_InstallationChecklist"> </a>

## <a name="installation-checklist"></a>Lista de comprobación de la instalación

El paquete de instalación del proveedor debe llevar a cabo una serie de comprobaciones de instalación, tal como se muestra en la figura 1, para asegurarse de que el proveedor se instala correctamente.
  
**En la figura 1. Lógica de instalación del proveedor**

![Lista de comprobación de la instalación](media/odc_ol14_ta_OSC_Fig07.gif)
  
El procedimiento siguiente describe las comprobaciones de la instalación que se describen en la figura 1.
  
1. Como requisito previo, detectar si Outlook está instalado o presentar y, si instalado o está presente, determine si la versión de Outlook admite la OSC. Para obtener más información acerca de la detección de la versión instalada de Outlook, vea [comprobar la versión de Outlook](http://msdn.microsoft.com/library/672fc380-a29b-4e99-9211-949fd5065723%28Office.15%29.aspx).
    
   - Si la versión de Outlook instalada es anterior a Outlook 2003, no se puede completar el procedimiento de instalación del proveedor. Informar al usuario para obtener una versión compatible de Outlook y el OSC antes de proceder a instalar al proveedor de OSC.
    
   - Si Outlook no está instalado, vaya al paso 2.
    
   - Si está instalado Outlook 2003 u Outlook 2007, vaya al paso 3. 
    
   - Si está instalado Outlook 2010 o Outlook 2013, vaya al paso 4.
    
2. **Continuar con este paso si Outlook no está instalado en el equipo cliente:**
    
   1. Compruebe si el OSC está instalado como un componente de forma predeterminada de una instalación de Click-to-Run de Outlook 2010 o Outlook 2013. Examine el `VirtualOutlook` clave en la siguiente ubicación en el registro de Windows: 
      
      - Para Outlook 2010,`HKEY_LOCAL_MACHINE\Software\Microsoft\Office\14.0\Common\InstallRoot\Virtual\VirtualOutlook`
      
      - Para Outlook Social Connector 2013,`HKEY_LOCAL_MACHINE\Software\Microsoft\Office\15.0\Common\InstallRoot\Virtual\VirtualOutlook`
      
      El `VirtualOutlook` clave es un valor REG_SZ que contiene la etiqueta de la configuración regional, como "en-us", del producto instalado. 
      
   2. Si el `VirtualOutlook` clave no existe, Outlook no está presente en el equipo cliente y no se puede completar el procedimiento de instalación del proveedor. Informar al usuario para obtener una versión compatible de Outlook y el OSC antes de proceder a instalar al proveedor de OSC. 
      
   3. Si el `VirtualOutlook` clave existe, Outlook se entregó mediante hacer clic y ejecutar en el equipo cliente. Continuar para comprobar la versión instalada de la biblioteca de tipos OSC examinando la `OSCVersion` clave en la siguiente ubicación en el registro de Windows: 
      
      `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\OSCVersion`
      
      El valor de `OSCVersion` es una cadena que especifica el número de versión de la biblioteca de tipos de Socialprovider.dll (por ejemplo, "1.0", "1.1" o "15"). 
      
   4. Si `OSCVersion` es "1.0", "1.1" o "15", que está instalada una versión adecuada de OSC. Vaya al paso 6 para encontrar la configuración regional actual de Outlook usuario interfaz para prepararse para instalar la versión más reciente de la OSC. 
      
   5. De lo contrario, `OSCVersion` no contiene un valor esperado. Vaya al paso 6 para encontrar la configuración regional actual de Outlook usuario interfaz para preparar para la instalación de una versión adecuada de la OSC. 
    
3. **Continuar con este paso si Outlook 2003 u Outlook 2007 está instalado en el equipo cliente:**
    
   1. Compruebe si está instalado la OSC mediante la escritura de un instalador de acción personalizada para probar la existencia del identificador del componente completo siguiente:
      
      `{A3B82DA3-8AD9-4935-AEA8-54B754459483}`
      
      El identificador del componente completo es un GUID que proporciona un método de direccionamiento indirecto de un solo nivel, similar a un puntero. Para obtener más información acerca de Windows Installer, vea la [Guía básica de documentación de Windows Installer](http://msdn.microsoft.com/library/_msi_roadmap_to_windows_installer_documentation.aspx).
      
   2. Si el componente completo especificado no existe, se instala una versión de la OSC. Vaya al paso 5 para encontrar la configuración regional actual de Outlook usuario interfaz para prepararse para instalar la versión más reciente de la OSC.
      
   3. De lo contrario, no se instala el OSC. Vaya al paso 6 para encontrar la configuración regional actual de Outlook usuario interfaz para preparar para la instalación de una versión adecuada de la OSC.
      
4. **Continuar con este paso si Outlook 2010 o 2013 de Outlook está instalado en el equipo cliente:**
    
   1. Determinar el valor de bits de la versión instalada de Outlook mediante el examen de la `Bitness` clave en la siguiente ubicación en el registro de Windows: 
      
      - Para Outlook 2010, examine`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\14.0\Outlook`
      
      - Para Outlook 2013, examine`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Outlook`
      
      El `Bitness` clave es "x86" para el Outlook de 32 bits, o "x64" para Outlook de 64 bits. 
      
   2. Si su proveedor es un proveedor administrado y compila el componente de proveedor que especifica la plataforma de destino como **Cualquier CPU**, continúe con el paso 6 para encontrar la configuración regional actual de Outlook usuario interfaz para prepararse para instalar la versión más reciente de la OSC. Su proveedor funcionará en las versiones de 32 bits y 64 bits de la OSC.
      
   3. Si su proveedor es un componente COM nativo, examine el valor de bits de la versión instalada de Outlook:
      
      - Si la versión de Outlook instalada es de 32 bits, tendrá el procedimiento de instalación instalar a un proveedor de 32 bits (en el paso 8), después de asegurarse de que está instalado un OSC adecuado.
      
      - De lo contrario, la versión de Outlook instalada es de 64 bits, y tendrá el procedimiento de instalación instalar a un proveedor de 64 bits (en el paso 8), después de asegurarse de que está instalado un OSC adecuado. 
      
   4. Continúe con el paso 6 para encontrar la configuración regional actual de Outlook usuario interfaz para preparar para la instalación de una versión adecuada de la OSC.
    
5. **Continuar con este paso si Outlook 2003 u Outlook 2007 está instalado y el OSC está instalado en el equipo cliente:** Comprobar la configuración regional actual interfaz de usuario de Outlook mediante el examen de la `OSCLcid` clave en la siguiente ubicación en el registro de Windows: 
    
   `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\OSCLcid`
    
   El `OSCLcid` clave es un valor DWORD que especifica la etiqueta de configuración regional de ingeniería de Internet (IETF) (definida por [[RFC4646]](http://www.ietf.org/rfc/rfc4646.txt) y [[RFC4647]](http://www.ietf.org/rfc/rfc4647.txt)), que representa la configuración regional actual interfaz de usuario de Outlook. Continúe con el paso 7 para instalar el OSC más reciente en el equipo cliente.
    
6. **Continuar con este paso si está instalado Outlook 2003 u Outlook 2007, o Outlook 2010 o Outlook 2013 está presente, pero el OSC más reciente no está necesariamente instalado en el equipo cliente:**
    
   Utilice el objeto **LanguageSettings** para determinar el LCID de la configuración regional la interfaz de usuario de Outlook. El siguiente fragmento de código de Visual Basic Scripting Edition (VBScript), muestra cómo obtener el LCID de la configuración regional la interfaz de usuario de Outlook. 
    
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

7. **Continuar con este paso si el programa de instalación tiene el LCID de la versión instalada de Outlook, pero el OSC más reciente no está necesariamente instalado en el equipo cliente:**
    
   Encadenamiento de un vínculo de g en el paquete de instalación para asegurarse de que la versión más reciente de la OSC está instalada en el equipo cliente. El formato de vínculo de g es como sigue:
    
   http://g.live.com/0CR_LCID_ /  _Glink_
    
   Consulte la tabla 1 a continuación para los valores _LCID_ admitidos y la tabla 2 para los valores de _Glink_ admitidos. Por ejemplo, el vínculo g para instalar la versión más reciente de la OSC de 32 bits para 32 bits Outlook Social Connector 2013 (inglés) es como sigue: 
    
   http://g.live.com/0CR1033/82
    
8. Instalación del proveedor. El procedimiento de instalación del proveedor debe registrar el identificador de programación (ProgID) en la ubicación del registro de Windows adecuada. Para obtener más información, vea [registrar un proveedor](registering-a-provider.md). Además, asegúrese de que el valor de bits del proveedor para instalarse es el mismo que el valor de bits de la versión de Outlook está presente en el equipo cliente. Por ejemplo, puede instalar un proveedor de 32 bits si está presente 2013 de Outlook de 32 bits y un proveedor de 64 bits si está instalado Outlook 2013 de 64 bits. Para Outlook 2003 o 2007, se aplica sólo la versión de 32 bits de su proveedor. 
    
**Tabla 1: Configuración regional compatible y los valores LCID correspondientes en hexadecimal para el OSC**
  
|**Configuración regional**|**LCID**|
|:-----|:-----|
|ar-sa  <br/> |1025  <br/> |
|bg-bg  <br/> |1026  <br/> |
|CA-es  <br/> |1027  <br/> |
|cs-cz  <br/> |1029  <br/> |
|da-dk  <br/> |1030  <br/> |
|de-de  <br/> |1031  <br/> |
|el-gr  <br/> |1032  <br/> |
|en-us  <br/> |1033  <br/> |
|es-es  <br/> |3082  <br/> |
|et-ee  <br/> |1061  <br/> |
|la Unión Europea-es  <br/> |1069  <br/> |
|fi-fi  <br/> |1035  <br/> |
|fr-fr  <br/> |1036  <br/> |
|Contabilidad-es  <br/> |1110  <br/> |
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
|SR-cyrl-cs  <br/> |3098  <br/> |
|SR-latn-cs  <br/> |2074  <br/> |
|sv-se  <br/> |1053  <br/> |
|th-th  <br/> |1054  <br/> |
|tr-tr  <br/> |1055  <br/> |
|uk-ua  <br/> |1058  <br/> |
|zh-cn  <br/> |2052  <br/> |
|zh-tw  <br/> |1028  <br/> |
   
**Tabla 2: Valores de Glink admitidos para el OSC**
  
|**Valor de GLINK**|**Funci�n**|
|:-----|:-----|
|80  <br/> |Instala la versión más reciente de OSC para Outlook 2003 u Outlook 2007.  <br/> |
|82  <br/> |Instala la revisión más reciente de 32 bits OSC para Outlook 2007, Outlook 2010 o Outlook Social Connector 2013.  <br/> |
|83  <br/> |Instala la revisión más reciente de OSC de 64 bits para Outlook 2010 o Outlook Social Connector 2013.  <br/> |
   
## <a name="see-also"></a>Vea también

- [Registrar un proveedor](registering-a-provider.md) 
- [Pasos rápidos para aprender a desarrollar un proveedor](quick-steps-for-learning-to-develop-a-provider.md)
- [Implementación de un proveedor](deploying-a-provider.md)

