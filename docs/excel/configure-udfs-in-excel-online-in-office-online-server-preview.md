---
title: Configurar udf en Excel Online en Office Online Server
manager: lindalu
ms.date: 12/03/2019
ms.audience: ITPro
localization_priority: Normal
ms.assetid: 3e0ca274-e9cd-48a1-8cfc-9d5053738972
description: Use funciones definidas por el usuario (UDF) en Excel Online en Office Online Server para llamar a funciones personalizadas.
ms.openlocfilehash: e1b005079c03ae3028ba6bf9ee1156c6ae2eae80
ms.sourcegitcommit: 007aa2ceb4f569201c3f4372de5c83b6c61f8875
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/02/2020
ms.locfileid: "43102936"
---
# <a name="configure-udfs-in-excel-online-in-office-online-server"></a>Configurar udf en Excel Online en Office Online Server

Use funciones definidas por el usuario (UDF) en Excel Online en Office Online Server para llamar a funciones personalizadas. 
  
Las funciones definidas por el usuario (UDF) en Excel Online permiten llamar a funciones personalizadas escritas en código administrado mediante fórmulas en celdas. Puede usar udf para:
  
- Llamar a funciones matemáticas personalizadas.
    
- Obtener datos de orígenes de datos personalizados en hojas de cálculo.
    
- Llamar a servicios web.
    
Puede instalar archivos binarios UDF en una de estas dos ubicaciones:
  
- Un directorio local. Por ejemplo: 
    
    C:\UDFs\MySampleUdf.dll
    
- La memoria caché de ensamblados global. Por ejemplo: 
    
    CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=en, PublicKeyToken=e8123117d7ba9ae38
    
Haga referencia a la ubicación cuando cree una **definición New-OfficeWebAppsExcelUserDefinedFunction** en Office Online Server. 
  
> [!NOTE]
> Office Online Server no admite UDF ubicadas en recursos compartidos de red. 
  
## <a name="enable-udfs-on-office-online-server"></a>Habilitar las UDF en Office Online Server 

Cuando un administrador crea una nueva granja de servidores de Office Web Apps Server mediante el cmdlet [New-OfficeWebAppsFarm](https://docs.microsoft.com/powershell/module/officewebapps/new-officewebappsfarm?view=officewebapps-ps) Windows PowerShell, los ensamblados UDF se deshabilitan de forma predeterminada. El valor predeterminado de la **marca ExcelUdfsAllowed** es false. 
  
Para habilitar las UDF, ejecute el siguiente comando Windows PowerShell en Office Online Server, una vez creada la granja de servidores de Office Web Apps Server.
  
`Set-OfficeWebAppsFarm - ExcelUdfsAllowed:$true`
  
## <a name="create-udf-definitions-on-office-online-server"></a>Crear definiciones de UDF en Office Online Server

Después de habilitar las UDF, debe crear una definición para el binario que contiene las UDF. Para crear una definición para el binario UDF en Office Online Server, use el cmdlet **New-OfficeWebAppsExcelUserDefinedFunction.** Este cmdlet incluye los siguientes parámetros: 
  
- **Ensamblado**
    
- **AssemblyLocation**
    
- **Habilitar** (se establece en False de forma predeterminada) 
    
- **Descripción**
    
En los ejemplos siguientes se muestra cómo crear las definiciones de UDF.
  
`New-OfficeWebAppsExcelUserDefinedFunction -Assembly c:\myudf.dll -AssemblyLocation LocalFile -Enable:$true -Description "My Server UDFs"`
  
`New-OfficeWebAppsExcelUserDefinedFunction -Assembly "CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=en, PublicKeyToken=e8123117d7ba9ae38" -AssemblyLocation GAC -Enable:$true -Description "My GAC Server UDFs"`
  
Después de crear la nueva referencia de UDF, ejecute **iisreset** en el servidor para seleccionar la referencia inmediatamente. 
  
## <a name="additional-office-online-server-udf-windows-powershell-commands"></a>Comandos Windows PowerShell UDF de Office Online Server adicionales

Use los siguientes cmdlets Windows PowerShell para trabajar con UDF:
  
- **Get-OfficeWebAppsExcelUserDefinedFunction** (sin parámetros obligatorios): devuelve una lista de definiciones de UDF configuradas en Office Online Server. 
    
- **Set- OfficeWebAppsExcelUserDefinedFunction** (parámetro identity obligatorio): establece las propiedades de las definiciones udF existentes. 
    
- **Remove-OfficeWebAppsExcelUserDefinedFunction** (parámetro identity obligatorio): quita las definiciones de UDF existentes. 
    
## <a name="udf-sample"></a>Muestra de UDF

El siguiente archivo de ejemplo proporciona un libro de ejemplo que usa una UDF y el binario UDF:
  
- [BooleanDataType.xlsx: ](https://download.microsoft.com/download/6/7/F/67F724FD-1186-4209-BFF1-FBFD99E959D9/User%20Defined%20Function%20Assemblies/BooleanDataType.xlsx)un libro de ejemplo que usa una UDF  
    
## <a name="see-also"></a>Consulte también

- [Configurar las opciones administrativas de Excel Online](https://docs.microsoft.com/officeonlineserver/configure-excel-online-administrative-settings)  
- [Office Online Server](https://docs.microsoft.com/officeonlineserver/office-online-server)
    

