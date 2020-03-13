# MaitreDEtail
MaitreDetail asp.net webform
Script SQL:
CREATE TABLE [dbo].[Class] (
    [Code] VARCHAR (20) NOT NULL,
    [Nom]  VARCHAR (50) NULL,
    PRIMARY KEY CLUSTERED ([Code] ASC)
);

///////////////////////////
CREATE TABLE [dbo].[Etudiants] (
    [CIN]   INT            NOT NULL,
    [Nom]   NVARCHAR (50)  NULL,
    [Photo] NVARCHAR (200) NULL,
    [Class] VARCHAR (20)   NULL,
    PRIMARY KEY CLUSTERED ([CIN] ASC),
    CONSTRAINT [FK_Etudiants_ToTable] FOREIGN KEY ([Class]) REFERENCES [dbo].[Class] ([Code])
);


