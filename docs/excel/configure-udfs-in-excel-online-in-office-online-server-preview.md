---
title: Configurar las UDF en Excel en línea en Office Online Server
manager: soliver
ms.date: 03/18/2016
ms.audience: ITPro
localization_priority: Normal
ms.assetid: 3e0ca274-e9cd-48a1-8cfc-9d5053738972
description: Utilizar funciones definidas por el usuario (UDF) de Excel en línea en Office Online Server para llamar a funciones personalizadas.
ms.openlocfilehash: dbba60a62a1a4783b47c3f1fe40a118dd8ed0d6d
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722791"
---
# <a name="configure-udfs-in-excel-online-in-office-online-server"></a>Configurar las UDF en Excel en línea en Office Online Server

Utilizar funciones definidas por el usuario (UDF) de Excel en línea en Office Online Server para llamar a funciones personalizadas. 
  
Funciones definidas por el usuario (UDF) de Excel Online permiten llamar a funciones personalizadas escritas en código administrado mediante el uso de las fórmulas en las celdas. Puede usar las UDF para:
  
- Llamar a funciones matemáticas personalizadas.
    
- Obtener datos de orígenes de datos personalizados en hojas de cálculo.
    
- Llamar a servicios web.
    
Puede instalar los archivos binarios UDF en una de estas dos ubicaciones:
  
- Un directorio local. Por ejemplo: 
    
    C:\UDFs\MySampleUdf.dll 
    
- La caché de ensamblados global. Por ejemplo: 
    
    CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=en, PublicKeyToken=e8123117d7ba9ae38
    
Hacer referencia a la ubicación cuando se crea una definición de **New-OfficeWebAppsExcelUserDefinedFunction** en el servidor de Office Online. 
  
> [!NOTE]
> Office Online Server no es compatible con UDF que se encuentra en recursos compartidos de red. 
  
## <a name="enable-udfs-on-office-online-server"></a>Habilitar las UDF en servidor de Office Online 

Cuando un administrador crea una nueva granja de servidores de Office Web Apps Server mediante el cmdlet [New-OfficeWebAppsFarm](https://technet.microsoft.com/en-us/library/jj219436.aspx) Windows PowerShell, los ensamblados de UDF están deshabilitados de forma predeterminada. El valor predeterminado de la marca de **ExcelUdfsAllowed** es false. 
  
Para habilitar las UDF, ejecute el siguiente comando de Windows PowerShell en el servidor de Office Online, después de haber creado la granja de servidores de Office Web Apps Server.
  
`Set-OfficeWebAppsFarm - ExcelUdfsAllowed:$true`
  
## <a name="create-udf-definitions-on-office-online-server"></a>Crear definiciones de las UDF en servidor de Office Online

Después de habilitar las UDF, debe crear una definición para el archivo binario que contiene las UDF. Para crear una definición para su UDF binario en el servidor en línea de Office, use el cmdlet **New-OfficeWebAppsExcelUserDefinedFunction** . Este cmdlet incluye los siguientes parámetros: 
  
- **Ensamblado**
    
- **UbicaciónDeEnsamblado**
    
- **Habilitar** (se establece en False de forma predeterminada) 
    
- **Descripción**
    
Los siguientes ejemplos muestran cómo crear las definiciones de UDF.
  
`New-OfficeWebAppsExcelUserDefinedFunction -Assembly c:\myudf.dll -AssemblyLocation LocalFile -Enable:$true -Description "My Server UDFs"`
  
`New-OfficeWebAppsExcelUserDefinedFunction -Assembly "CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=en, PublicKeyToken=e8123117d7ba9ae38" -AssemblyLocation GAC -Enable:$true -Description "My GAC Server UDFs"`
  
Después de crear la nueva referencia UDF, ejecute **iisreset** en el servidor para seleccionar la referencia inmediatamente. 
  
## <a name="additional-office-online-server-udf-windows-powershell-commands"></a>Comandos de Windows PowerShell en Office Online Server UDF adicionales

Use los siguientes cmdlets de Windows PowerShell para trabajar con las UDF:
  
- **Get-OfficeWebAppsExcelUserDefinedFunction** (sin parámetros obligatorios) - devuelve una lista de definiciones de UDF que están configurados en el servidor de Office Online. 
    
- **Set-OfficeWebAppsExcelUserDefinedFunction** (El parámetro identity requiere) - establece las propiedades en las definiciones de UDF existentes. 
    
- **Remove-OfficeWebAppsExcelUserDefinedFunction** (El parámetro identity requiere) - quita las definiciones de UDF existentes. 
    
## <a name="udf-sample"></a>Ejemplo UDF

Los siguientes archivos proporcionan un libro de ejemplo que usa una UDF y el archivo UDF binario:
  
- [BooleanDataType.xlsx](https://download.microsoft.com/download/6/7/F/67F724FD-1186-4209-BFF1-FBFD99E959D9/User%20Defined%20Function%20Assemblies/BooleanDataType.xlsx): un libro de ejemplo que usa una UDF  
- [EcsUdfsCommonSet.dll](https://www.microsoft.com/en-us/search/result.aspx?q=EcsUdfsCommonSet.dll): el archivo binario UDF 
    
## <a name="see-also"></a>Consulte también

- [Configurar las opciones administrativas Excel Online](https://docs.microsoft.com/officeonlineserver/configure-excel-online-administrative-settings)  
- [Office Online Server](https://docs.microsoft.com/officeonlineserver/office-online-server)
    

