---
title: Muestra de proveedor de libreta de direcciones
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2ccf1643-5604-4fee-92cc-3d6af00e7f98
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: fa2a447d0757e75c95d7dc3d9b1dd16b8c7a8084
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25394723"
---
# <a name="address-book-provider-sample"></a>Muestra de proveedor de libreta de direcciones

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
En este ejemplo es compatible con un único contenedor de sólo lectura para los nombres para mostrar y direcciones de correo electrónico, que se leen de un archivo binario de plano. En el ejemplo es compatible con las plantillas de uso único y todas las opciones de configuración, excepto el Asistente para perfiles.
  
Puede descargar este ejemplo de [Ejemplos de código de API de mensajería de Outlook (MAPI)](https://go.microsoft.com/fwlink/?LinkId=129740
).
  
|||
|:-----|:-----|
|Archivo ejecutable:  <br/> |SABP32.dll  <br/> |
| Directorio de origen del código:  <br/> |SampleAddressBookProvider\SABP  <br/> |
|Idioma:  <br/> |C++  <br/> |
|Plataformas:  <br/> |Microsoft Visual Studio 2008 para compilar para Windows Vista, Windows Server 2008, Windows XP SP2 y Windows Server 2003 SP1  <br/> |
   
## <a name="supported-features"></a>Características admitidas

En este ejemplo es compatible con las siguientes características:
  
- Restricciones de tabla. El ejemplo implementa la resolución de coincidencia de prefijo y nombre ambiguo. No implementa el lenguaje de restricción de MAPI completo y restricciones se admiten sólo en el nombre para mostrar.
    
- Una tabla de para mostrar detalles para los usuarios de mensajería. 
    
- Direcciones de uso único.
    
- Un cuadro de diálogo Búsqueda avanzada.
    
- Un [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) interfaz. Parcialmente es compatible con esta interfaz; sus métodos **IMAPIProp** se delegan a la interfaz **IPropData** . Para obtener más información, vea el [IPropData: IMAPIProp](ipropdataimapiprop.md) interfaz. 
    
- Configuración interactiva y mediante programación.
    
## <a name="unsupported-features"></a>Características no admitidas

En este ejemplo no es compatible con las siguientes características:
  
- Ordenación.
    
- Listas de distribución.
    
- Crear, eliminar y modificar las entradas.
    
- Propiedades con varios valores.
    
- Propiedades con nombre.
    
- Distinción entre los nombres y el apellido en nombres para mostrar.
    
 **Para instalar al proveedor de la libreta de direcciones de ejemplo**
  
1. Para descargar el proveedor de la libreta de direcciones de ejemplo, consulte [descargar los ejemplos de MAPI de Outlook](downloading-the-outlook-mapi-samples.md).
    
2. Busque la carpeta donde guardó los ejemplos de MAPI de Outlook. Haga clic en el **OutlookMAPISamples -\<número de versión\> ** zip carpeta y haga clic en **Extraer todos**.
    
3. Haga clic en **Examinar**, seleccione la ubicación donde desea guardar el ejemplo y haga clic en **extraer**.
    
4. Ejecute Visual Studio 2008.
    
5. En Visual Studio 2008, haga clic en **archivo**, seleccione **Abrir**y, a continuación, haga clic en **Proyecto o solución**.
    
6. Vaya a la ubicación donde guardó el ejemplo, haga clic en **SABP.vcproj**y, a continuación, haga clic en **Abrir**.
    
7. On the **Build** menu, click **Build Solution**.
    
8. En el cuadro de diálogo **Guardar archivo como** , haga clic en **Guardar**.
    
9. En la carpeta donde guardó el ejemplo, haga clic en el archivo **install.bat** y haga clic en **Ejecutar como administrador**.
    
10. En el cuadro de diálogo **Control de cuentas de usuario** , haga clic en **continuar**.
    
    > [!NOTE]
    > **Install.bat** copia el archivo .dll en la carpeta de instalación de Microsoft Office de forma predeterminada, C:\Program Files\Microsoft Office\Office12\. Si ha instalado productos de Office en una ubicación diferente, haga clic en **Install.bat** y haga clic en **Editar**. El archivo se abre en el Bloc de notas. Reemplace la ruta de instalación predeterminada con la ruta de instalación utilizada en el equipo. 
  

